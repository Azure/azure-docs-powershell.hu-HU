---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479690"
---
# <span data-ttu-id="52846-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52846-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="52846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52846-102">SYNOPSIS</span></span>
<span data-ttu-id="52846-103">Adatkapcsolat frissítése</span><span class="sxs-lookup"><span data-stu-id="52846-103">Update a Data Connector.</span></span>

## <span data-ttu-id="52846-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="52846-104">SYNTAX</span></span>

### <span data-ttu-id="52846-105">DataConnectorId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52846-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52846-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="52846-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52846-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52846-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52846-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="52846-108">DESCRIPTION</span></span>
<span data-ttu-id="52846-109">Az **Update-AzSentinelDataConnector** parancsmag frissíti az adatösszekötőt a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="52846-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="52846-110">A **DataConnector-objektumokat** paraméterként vagy a folyamat műveleti jelének használatával is átadhatja, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="52846-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="52846-111">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="52846-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="52846-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="52846-112">EXAMPLES</span></span>

### <span data-ttu-id="52846-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="52846-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="52846-114">A parancs leállítja a Data Connector by *DataConnectorId* parancsot, és letiltja a *riasztások* *állapotát.*</span><span class="sxs-lookup"><span data-stu-id="52846-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="52846-115">Minden más tulajdonság változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="52846-115">All other properties remain the same.</span></span>

## <span data-ttu-id="52846-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52846-116">PARAMETERS</span></span>

### <span data-ttu-id="52846-117">-Riasztások</span><span class="sxs-lookup"><span data-stu-id="52846-117">-Alerts</span></span>
<span data-ttu-id="52846-118">Adatkapcsolat-összekötők riasztásai</span><span class="sxs-lookup"><span data-stu-id="52846-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="52846-119">-AwsRoleArn</span></span>
<span data-ttu-id="52846-120">Data Connector AWS Role Arn</span><span class="sxs-lookup"><span data-stu-id="52846-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="52846-121">-DataConnectorId</span></span>
<span data-ttu-id="52846-122">Adatkapcsolat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="52846-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52846-123">-DefaultProfile</span></span>
<span data-ttu-id="52846-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52846-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="52846-125">-DiscoveryLogs</span></span>
<span data-ttu-id="52846-126">Adatkapcsolat feltárási naplói</span><span class="sxs-lookup"><span data-stu-id="52846-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="52846-127">-Exchange</span></span>
<span data-ttu-id="52846-128">Adatcsatlakozó – Exchange</span><span class="sxs-lookup"><span data-stu-id="52846-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-129">-Indicators</span><span class="sxs-lookup"><span data-stu-id="52846-129">-Indicators</span></span>
<span data-ttu-id="52846-130">Adatkapcsolatjelzők</span><span class="sxs-lookup"><span data-stu-id="52846-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52846-131">-InputObject</span></span>
<span data-ttu-id="52846-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="52846-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52846-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="52846-133">-Logs</span></span>
<span data-ttu-id="52846-134">Adatcsatlakozó-naplók</span><span class="sxs-lookup"><span data-stu-id="52846-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52846-135">-ResourceGroupName</span></span>
<span data-ttu-id="52846-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="52846-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52846-137">-ResourceId</span></span>
<span data-ttu-id="52846-138">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="52846-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52846-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="52846-139">-SharePoint</span></span>
<span data-ttu-id="52846-140">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="52846-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52846-141">-SubscriptionId</span></span>
<span data-ttu-id="52846-142">Adatcsatlakozó előfizetésazonosítója</span><span class="sxs-lookup"><span data-stu-id="52846-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52846-143">-WorkspaceName</span></span>
<span data-ttu-id="52846-144">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="52846-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52846-145">-Confirm</span></span>
<span data-ttu-id="52846-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="52846-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52846-147">-WhatIf</span></span>
<span data-ttu-id="52846-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="52846-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52846-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52846-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52846-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52846-150">CommonParameters</span></span>
<span data-ttu-id="52846-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52846-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52846-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52846-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52846-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52846-153">INPUTS</span></span>

### <span data-ttu-id="52846-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52846-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="52846-155">System.String</span><span class="sxs-lookup"><span data-stu-id="52846-155">System.String</span></span>

## <span data-ttu-id="52846-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52846-156">OUTPUTS</span></span>

### <span data-ttu-id="52846-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="52846-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="52846-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="52846-158">NOTES</span></span>

## <span data-ttu-id="52846-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52846-159">RELATED LINKS</span></span>
