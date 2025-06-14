/*
  GitHub Repository: DLP-BGP-IAM-Threat-Project
  Description: Portfolio project demonstrating detection and prevention of insider threats through Data Loss Prevention (DLP), Identity and Access Management (IAM), and Border Gateway Protocol (BGP) anomaly detection.
*/

import { Card, CardContent } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { Button } from "@/components/ui/button";
import { Tabs, TabsList, TabsTrigger, TabsContent } from "@/components/ui/tabs";

export default function ProjectOverview() {
  return (
    <div className="p-6 space-y-6">
      <h1 className="text-4xl font-extrabold text-purple-600">🔐 Insider Threat Simulation Project</h1>
      <p className="text-lg text-gray-700">
        Detect and mitigate internal threats by combining <span className="text-red-500 font-semibold">Data Loss Prevention</span>,
        <span className="text-blue-500 font-semibold"> IAM policies</span>, and <span className="text-green-600 font-semibold">BGP anomaly detection</span>.
      </p>

      <Tabs defaultValue="dlp">
        <TabsList className="bg-gray-100 dark:bg-gray-800 border p-1 rounded-xl">
          <TabsTrigger value="dlp" className="text-red-500">DLP</TabsTrigger>
          <TabsTrigger value="iam" className="text-blue-500">IAM</TabsTrigger>
          <TabsTrigger value="bgp" className="text-green-600">BGP</TabsTrigger>
        </TabsList>

        <TabsContent value="dlp">
          <Card>
            <CardContent className="space-y-2 p-4">
              <h2 className="text-xl font-bold text-red-500">📁 DLP Module</h2>
              <p>Tool: <strong>Wazuh</strong></p>
              <p>Monitors and blocks sensitive file transfers such as SSNs or banking data.</p>
              <p className="bg-red-100 text-red-900 p-2 rounded-md">Sample Log:</p>
              <pre className="bg-gray-800 text-green-400 p-3 rounded-lg overflow-x-auto">
2025-06-01 14:34:02 | ALERT | File Transfer Detected: Employee_SSNs.docx | User: intern-usr01 | Action: Blocked</pre>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="iam">
          <Card>
            <CardContent className="space-y-2 p-4">
              <h2 className="text-xl font-bold text-blue-500">🔐 IAM Simulation</h2>
              <p>Tool: <strong>Keycloak</strong></p>
              <p>Shows role escalation and misconfigured access.</p>
              <p className="bg-blue-100 text-blue-900 p-2 rounded-md">Sample Log:</p>
              <pre className="bg-gray-800 text-yellow-300 p-3 rounded-lg overflow-x-auto">
2025-06-01 15:12:48 | POLICY BREACH | User: intern-usr01 | Escalated Access to Resource: Admin_DB | Result: Unauthorized Access</pre>
            </CardContent>
          </Card>
        </TabsContent>

        <TabsContent value="bgp">
          <Card>
            <CardContent className="space-y-2 p-4">
              <h2 className="text-xl font-bold text-green-600">🌐 BGP Monitoring</h2>
              <p>Tool: <strong>BGPalerter</strong></p>
              <p>Detects route hijacks and anomalous BGP behavior.</p>
              <p className="bg-green-100 text-green-900 p-2 rounded-md">Sample Alert:</p>
              <pre className="bg-gray-800 text-pink-400 p-3 rounded-lg overflow-x-auto">
2025-06-01 16:27:13 | ALERT | Possible BGP Hijack Detected | Prefix: 192.0.2.0/24 | AS Path: AS64501 > AS12345 (Unexpected)</pre>
            </CardContent>
          </Card>
        </TabsContent>
      </Tabs>

      <div className="bg-yellow-50 p-4 border-l-4 border-yellow-400 text-yellow-800 mt-6">
        <p className="font-medium">📝 Project Summary:</p>
        <p>
          This lab simulates insider threats where an intern tries to exfiltrate sensitive files,
          IAM role misuse grants unauthorized access, and BGP hijacks are detected to protect outbound data routes.
        </p>
      </div>

      <div className="mt-6">
        <Button className="bg-gradient-to-r from-red-500 via-purple-500 to-blue-500 text-white font-bold py-2 px-4 rounded-full">
          View Full Logs and Reports
        </Button>
      </div>
    </div>
  );
}
