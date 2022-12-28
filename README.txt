PATCH FOR APAR         : JR59080
PATCH NAME             : patch_JR59080_DFD_server_11700
ENGINEERING TEAM       : DataStage Flow Designer
COMPONENT              : DFD
TIERS                  : server, engine
OPERATING SYSTEM       : All
SUITE VERSION*         : 11.7.0.0
UNINSTALL**            : Unsupported
PREREQUISITE PATCHES   : None
COREQUISITE PATCHES    : None
PRE-INSTALL STEPS      : None
SPECIFIC INSTALL STEPS : None
POST-INSTALL STEPS     : None
RECOMPILE JOBS         : Not Required

  * This patch requires that IBM Information Server suite and component be 
    installed at the exact level shown and no other.

 ** IMPORTANT: if the patch cannot be uninstalled, you must back up your system
    prior to installing the patch. Backups are recommended prior to all patch installs.
    The patch installation instructions below include information on backups and uninstalling.

RESOLVED ISSUES: 
JR59080: Add access per user roles and missing Kafka properties in DataStage Flow Designer.

INSTALLATION INSTRUCTIONS:
=========================
  Generic patch installation instructions are available with this download and
  are also available separately here; use the link appropriate for this patch version:
  
  http://www-01.ibm.com/support/docview.wss?uid=swg27050613 

DATASTAGE FLOW DESIGNER PATCH INSTRUCTIONS:
===========================================
	This patch includes to both Services tier and Engine tier. DataStage Flow Designer does not have any client side installation software.
	For single tier installations, apply this patch on the single tier machine following the patch instruction. 
	For multi-tier installations, apply this patch to the services tier and engine tier following the patch instructions.
	Make sure to back-up patched files listed in below section for any Rollbacks. 
	
PATCHED FILES: 
==============
  This patch modifies the following files, shown from the root of the IBM 
  Information Server installation.
  Services:

	  <IS-Install-Path>/wlp/usr/server/iis/apps/dscdesigner/dscdesigner.war
	  <IS-Install-Path>/wlp/usr/server/iis/apps/dscdesignerapi/dscdesignerapi.war
  
  Engine:
	
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/CognitionJettyEngine.jar
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/JettyServer/conf/cognition_engine_jetty.properties
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/JettyServer/conf/log4j2.xml
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/JettyServer/conf/log4j.dtd
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/JettyServer/SSLSetup/cognitionjetty.p12
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/JettyServer/SSLSetup/keystore
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/stopCognitiveDesignerServer.sh   (UNIX/Linux)
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/startCognitiveDesignerServer.sh  (UNIX/Linux)
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/stopCognitiveDesignerServer.bat  (Windows)
	  <IS-Install-Path>/ASBNode/CognitiveDesignerEngine/startCognitiveDesignerServer.bat (Windows)
	  
SUPPORT POLICY STATEMENT FOR FIX PACKS AND PATCHES:
==================================================
  The following document describes the role and purpose of IBM InfoSphere 
  Information Server fix packs and patches.
  
  http://www-01.ibm.com/support/docview.wss?uid=swg27037015
