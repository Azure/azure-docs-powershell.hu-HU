---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017469"
---
# <span data-ttu-id="0973b-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0973b-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="0973b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0973b-102">SYNOPSIS</span></span>
<span data-ttu-id="0973b-103">Létrehozza a szinapszis-elemzési tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="0973b-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="0973b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0973b-104">SYNTAX</span></span>

### <span data-ttu-id="0973b-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0973b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0973b-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="0973b-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0973b-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0973b-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0973b-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="0973b-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0973b-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="0973b-109">DESCRIPTION</span></span>
<span data-ttu-id="0973b-110">A **New-AzSynapseFirewallRule** parancsmag az Azure szinapszis Analytics-tűzfalszabályok létrehozására szolgáló szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0973b-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="0973b-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0973b-111">EXAMPLES</span></span>

### <span data-ttu-id="0973b-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0973b-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="0973b-113">Ez a parancs a ContosoFirewallRule nevű tűzfal-szabályt hoz létre a ContosoFirewallRule nevű munkaterület-ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="0973b-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="0973b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0973b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="0973b-115">A parancs létrehoz egy ContosoFirewallRule nevű tűzfal-szabályt a munkaterületen keresztül csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="0973b-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="0973b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="0973b-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="0973b-117">Ez a parancs tűzfal-szabályt hoz létre, amely lehetővé teszi az összes Azure IPS beállítását egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="0973b-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="0973b-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0973b-118">PARAMETERS</span></span>

### <span data-ttu-id="0973b-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="0973b-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="0973b-120">Speciális tűzfalszabályok létrehozása, amely lehetővé teszi az összes Azure IPs hozzáférését.</span><span class="sxs-lookup"><span data-stu-id="0973b-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="0973b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0973b-121">-AsJob</span></span>
<span data-ttu-id="0973b-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="0973b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0973b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0973b-123">-DefaultProfile</span></span>
<span data-ttu-id="0973b-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0973b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0973b-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0973b-125">-EndIpAddress</span></span>
<span data-ttu-id="0973b-126">A tűzfalszabály záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="0973b-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="0973b-127">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0973b-127">Must be IPv4 format.</span></span>
<span data-ttu-id="0973b-128">Nagyobbnak vagy egyenlőnek kell lennie a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="0973b-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="0973b-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0973b-129">-Name</span></span>
<span data-ttu-id="0973b-130">A firerwall szabály neve a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="0973b-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="0973b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0973b-131">-ResourceGroupName</span></span>
<span data-ttu-id="0973b-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="0973b-132">Resource group name.</span></span>

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

### <span data-ttu-id="0973b-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0973b-133">-StartIpAddress</span></span>
<span data-ttu-id="0973b-134">A tűzfalszabály kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="0973b-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="0973b-135">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="0973b-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="0973b-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0973b-136">-WorkspaceName</span></span>
<span data-ttu-id="0973b-137">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="0973b-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0973b-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0973b-138">-WorkspaceObject</span></span>
<span data-ttu-id="0973b-139">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="0973b-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0973b-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0973b-140">-Confirm</span></span>
<span data-ttu-id="0973b-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0973b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0973b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0973b-142">-WhatIf</span></span>
<span data-ttu-id="0973b-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0973b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0973b-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0973b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0973b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0973b-145">CommonParameters</span></span>
<span data-ttu-id="0973b-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0973b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0973b-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0973b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0973b-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0973b-148">INPUTS</span></span>

### <span data-ttu-id="0973b-149">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0973b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0973b-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0973b-150">OUTPUTS</span></span>

### <span data-ttu-id="0973b-151">Microsoft. Azure. commands. szinapszis. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0973b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="0973b-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0973b-152">NOTES</span></span>

## <span data-ttu-id="0973b-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0973b-153">RELATED LINKS</span></span>
