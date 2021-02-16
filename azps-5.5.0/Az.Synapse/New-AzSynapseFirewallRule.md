---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164571"
---
# <span data-ttu-id="4eaed-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4eaed-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="4eaed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eaed-102">SYNOPSIS</span></span>
<span data-ttu-id="4eaed-103">Létrehozza a Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="4eaed-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="4eaed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4eaed-104">SYNTAX</span></span>

### <span data-ttu-id="4eaed-105">CreateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4eaed-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eaed-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eaed-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4eaed-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eaed-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4eaed-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="4eaed-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eaed-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4eaed-109">DESCRIPTION</span></span>
<span data-ttu-id="4eaed-110">A **New-AzSynapseFirewallRule parancsmag** létrehoz egy Azure Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="4eaed-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="4eaed-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4eaed-111">EXAMPLES</span></span>

### <span data-ttu-id="4eaed-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="4eaed-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="4eaed-113">Ez a parancs létrehozza a ContosoFirewallRule nevű tűzfalszabályt a ContosoWorkspace munkaterületen ContosoFirewallRule néven.</span><span class="sxs-lookup"><span data-stu-id="4eaed-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="4eaed-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="4eaed-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="4eaed-115">Ez a parancs létrehozza a ContosoFirewallRule nevű tűzfalszabályt egy munkaterületen keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="4eaed-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="4eaed-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="4eaed-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="4eaed-117">Ez a parancs olyan tűzfalszabályt hoz létre, amely engedélyezi az összes Azure IP-címet egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="4eaed-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="4eaed-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eaed-118">PARAMETERS</span></span>

### <span data-ttu-id="4eaed-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="4eaed-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="4eaed-120">Létrehoz egy speciális tűzfalszabályt, amely engedélyezi az összes Azure IP-nek a hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="4eaed-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="4eaed-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4eaed-121">-AsJob</span></span>
<span data-ttu-id="4eaed-122">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4eaed-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4eaed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eaed-123">-DefaultProfile</span></span>
<span data-ttu-id="4eaed-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4eaed-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eaed-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="4eaed-125">-EndIpAddress</span></span>
<span data-ttu-id="4eaed-126">A tűzfalszabály ip-címe.</span><span class="sxs-lookup"><span data-stu-id="4eaed-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="4eaed-127">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4eaed-127">Must be IPv4 format.</span></span>
<span data-ttu-id="4eaed-128">A startIpAddress értéknél nem kisebbnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4eaed-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="4eaed-129">-Name</span><span class="sxs-lookup"><span data-stu-id="4eaed-129">-Name</span></span>
<span data-ttu-id="4eaed-130">A munkaterület firerwall-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="4eaed-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="4eaed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eaed-131">-ResourceGroupName</span></span>
<span data-ttu-id="4eaed-132">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4eaed-132">Resource group name.</span></span>

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

### <span data-ttu-id="4eaed-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="4eaed-133">-StartIpAddress</span></span>
<span data-ttu-id="4eaed-134">A tűzfalszabály kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="4eaed-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="4eaed-135">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4eaed-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="4eaed-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4eaed-136">-WorkspaceName</span></span>
<span data-ttu-id="4eaed-137">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4eaed-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4eaed-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4eaed-138">-WorkspaceObject</span></span>
<span data-ttu-id="4eaed-139">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="4eaed-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4eaed-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eaed-140">-Confirm</span></span>
<span data-ttu-id="4eaed-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4eaed-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eaed-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eaed-142">-WhatIf</span></span>
<span data-ttu-id="4eaed-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4eaed-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eaed-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4eaed-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eaed-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eaed-145">CommonParameters</span></span>
<span data-ttu-id="4eaed-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eaed-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eaed-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eaed-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eaed-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eaed-148">INPUTS</span></span>

### <span data-ttu-id="4eaed-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4eaed-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4eaed-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4eaed-150">OUTPUTS</span></span>

### <span data-ttu-id="4eaed-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4eaed-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="4eaed-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4eaed-152">NOTES</span></span>

## <span data-ttu-id="4eaed-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4eaed-153">RELATED LINKS</span></span>
