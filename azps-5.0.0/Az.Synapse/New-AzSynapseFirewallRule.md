---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302318"
---
# <span data-ttu-id="06194-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06194-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="06194-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06194-102">SYNOPSIS</span></span>
<span data-ttu-id="06194-103">Létrehozza a szinapszis-elemzési tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="06194-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="06194-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06194-104">SYNTAX</span></span>

### <span data-ttu-id="06194-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06194-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06194-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="06194-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06194-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06194-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06194-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="06194-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06194-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="06194-109">DESCRIPTION</span></span>
<span data-ttu-id="06194-110">A **New-AzSynapseFirewallRule** parancsmag az Azure szinapszis Analytics-tűzfalszabályok létrehozására szolgáló szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="06194-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="06194-111">Példák</span><span class="sxs-lookup"><span data-stu-id="06194-111">EXAMPLES</span></span>

### <span data-ttu-id="06194-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06194-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="06194-113">Ez a parancs a ContosoFirewallRule nevű tűzfal-szabályt hoz létre a ContosoFirewallRule nevű munkaterület-ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="06194-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="06194-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="06194-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="06194-115">A parancs létrehoz egy ContosoFirewallRule nevű tűzfal-szabályt a munkaterületen keresztül csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="06194-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="06194-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="06194-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="06194-117">Ez a parancs tűzfal-szabályt hoz létre, amely lehetővé teszi az összes Azure IPS beállítását egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="06194-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="06194-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06194-118">PARAMETERS</span></span>

### <span data-ttu-id="06194-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="06194-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="06194-120">Speciális tűzfalszabályok létrehozása, amely lehetővé teszi az összes Azure IPs hozzáférését.</span><span class="sxs-lookup"><span data-stu-id="06194-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06194-121">-AsJob</span></span>
<span data-ttu-id="06194-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="06194-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06194-123">-DefaultProfile</span></span>
<span data-ttu-id="06194-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06194-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06194-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="06194-125">-EndIpAddress</span></span>
<span data-ttu-id="06194-126">A tűzfalszabály záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="06194-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="06194-127">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="06194-127">Must be IPv4 format.</span></span>
<span data-ttu-id="06194-128">Nagyobbnak vagy egyenlőnek kell lennie a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="06194-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06194-129">-Name</span></span>
<span data-ttu-id="06194-130">A firerwall szabály neve a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="06194-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06194-131">-ResourceGroupName</span></span>
<span data-ttu-id="06194-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="06194-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="06194-133">-StartIpAddress</span></span>
<span data-ttu-id="06194-134">A tűzfalszabály kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="06194-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="06194-135">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="06194-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="06194-136">-WorkspaceName</span></span>
<span data-ttu-id="06194-137">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="06194-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06194-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="06194-138">-WorkspaceObject</span></span>
<span data-ttu-id="06194-139">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="06194-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06194-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06194-140">-Confirm</span></span>
<span data-ttu-id="06194-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06194-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06194-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06194-142">-WhatIf</span></span>
<span data-ttu-id="06194-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06194-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06194-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06194-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06194-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06194-145">CommonParameters</span></span>
<span data-ttu-id="06194-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06194-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06194-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06194-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06194-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06194-148">INPUTS</span></span>

### <span data-ttu-id="06194-149">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="06194-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="06194-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06194-150">OUTPUTS</span></span>

### <span data-ttu-id="06194-151">Microsoft. Azure. commands. szinapszis. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06194-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="06194-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06194-152">NOTES</span></span>

## <span data-ttu-id="06194-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06194-153">RELATED LINKS</span></span>
