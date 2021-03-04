---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 7eb4675e44a252feec913b531a30f9062f6b791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930786"
---
# <span data-ttu-id="805b1-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="805b1-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="805b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="805b1-102">SYNOPSIS</span></span>
<span data-ttu-id="805b1-103">Hozzon létre egy adatkapcsolat-összekötőt.</span><span class="sxs-lookup"><span data-stu-id="805b1-103">Create a Data Connector.</span></span>

## <span data-ttu-id="805b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="805b1-104">SYNTAX</span></span>

### <span data-ttu-id="805b1-105">AzureActiveDirectory (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="805b1-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="805b1-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="805b1-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="805b1-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-108">AmazonWebServicesCloudTweb</span><span class="sxs-lookup"><span data-stu-id="805b1-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="805b1-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="805b1-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-111">Office365</span><span class="sxs-lookup"><span data-stu-id="805b1-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="805b1-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="805b1-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="805b1-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="805b1-113">DESCRIPTION</span></span>
<span data-ttu-id="805b1-114">A **New-AzSentinelAlertRule** parancsmag létrehoz egy analytic (riasztási szabály) a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="805b1-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="805b1-115">A létrehozható riasztási szabály fajtáját meg kell adnia az egyik paraméternek, például az -AzureActiveDirectorynak.</span><span class="sxs-lookup"><span data-stu-id="805b1-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="805b1-116">Minden egyes típusúhoz különböző kötelező paramétereket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="805b1-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="805b1-117">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="805b1-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="805b1-118">Megjegyzés: A portálon nem minden adatkapcsolat érhető el API-n keresztül.</span><span class="sxs-lookup"><span data-stu-id="805b1-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="805b1-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="805b1-119">EXAMPLES</span></span>

### <span data-ttu-id="805b1-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="805b1-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="805b1-121">Ebben a példában létrehoz egy **DataConnectort** az Azure Biztonsági központhoz a megadott munkaterületen, majd azt egy másik $DataConnector tárolja.</span><span class="sxs-lookup"><span data-stu-id="805b1-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="805b1-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="805b1-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="805b1-123">Ebben a példában létrehoz egy **DataConnectort** a Microsoft Cloud App Security szolgáltatáshoz a megadott munkaterületen, majd azt a $DataConnector tárolja.</span><span class="sxs-lookup"><span data-stu-id="805b1-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="805b1-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="805b1-124">PARAMETERS</span></span>

### <span data-ttu-id="805b1-125">-Riasztások</span><span class="sxs-lookup"><span data-stu-id="805b1-125">-Alerts</span></span>
<span data-ttu-id="805b1-126">Adatkapcsolat-összekötők riasztásai</span><span class="sxs-lookup"><span data-stu-id="805b1-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-127">-AmazonWebServicesCloudTweb</span><span class="sxs-lookup"><span data-stu-id="805b1-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="805b1-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="805b1-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="805b1-129">-AwsRoleArn</span></span>
<span data-ttu-id="805b1-130">Data Connector AWS Role Arn</span><span class="sxs-lookup"><span data-stu-id="805b1-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="805b1-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="805b1-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="805b1-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="805b1-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="805b1-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="805b1-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="805b1-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="805b1-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="805b1-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="805b1-137">-DataConnectorId</span></span>
<span data-ttu-id="805b1-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="805b1-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805b1-139">-DefaultProfile</span></span>
<span data-ttu-id="805b1-140">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="805b1-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="805b1-141">-DiscoveryLogs</span></span>
<span data-ttu-id="805b1-142">Adatkapcsolat feltárási naplói</span><span class="sxs-lookup"><span data-stu-id="805b1-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="805b1-143">-Exchange</span></span>
<span data-ttu-id="805b1-144">Adatcsatlakozó – Exchange</span><span class="sxs-lookup"><span data-stu-id="805b1-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-145">-Indicators</span><span class="sxs-lookup"><span data-stu-id="805b1-145">-Indicators</span></span>
<span data-ttu-id="805b1-146">Adatkapcsolatjelzők</span><span class="sxs-lookup"><span data-stu-id="805b1-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="805b1-147">-Logs</span></span>
<span data-ttu-id="805b1-148">Adatcsatlakozó-naplók</span><span class="sxs-lookup"><span data-stu-id="805b1-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="805b1-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="805b1-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="805b1-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="805b1-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="805b1-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="805b1-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="805b1-153">-Office365</span></span>
<span data-ttu-id="805b1-154">Data Connector Office 365</span><span class="sxs-lookup"><span data-stu-id="805b1-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="805b1-155">-ResourceGroupName</span></span>
<span data-ttu-id="805b1-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="805b1-156">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="805b1-157">-SharePoint</span></span>
<span data-ttu-id="805b1-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="805b1-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="805b1-159">-SubscriptionId</span></span>
<span data-ttu-id="805b1-160">Adatcsatlakozó előfizetésazonosítója</span><span class="sxs-lookup"><span data-stu-id="805b1-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="805b1-161">-ThreatIntelligence</span></span>
<span data-ttu-id="805b1-162">Adatcsatlakozó veszélyforrás-felderítés</span><span class="sxs-lookup"><span data-stu-id="805b1-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="805b1-163">-WorkspaceName</span></span>
<span data-ttu-id="805b1-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="805b1-164">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="805b1-165">-Confirm</span></span>
<span data-ttu-id="805b1-166">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="805b1-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805b1-167">-WhatIf</span></span>
<span data-ttu-id="805b1-168">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="805b1-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="805b1-169">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="805b1-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="805b1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805b1-170">CommonParameters</span></span>
<span data-ttu-id="805b1-171">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805b1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805b1-172">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="805b1-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805b1-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="805b1-173">INPUTS</span></span>

### <span data-ttu-id="805b1-174">Nincs</span><span class="sxs-lookup"><span data-stu-id="805b1-174">None</span></span>
## <span data-ttu-id="805b1-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="805b1-175">OUTPUTS</span></span>

### <span data-ttu-id="805b1-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="805b1-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="805b1-177">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="805b1-177">NOTES</span></span>

## <span data-ttu-id="805b1-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="805b1-178">RELATED LINKS</span></span>
