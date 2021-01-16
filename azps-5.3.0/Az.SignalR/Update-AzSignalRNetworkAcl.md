---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479509"
---
# <span data-ttu-id="83e7a-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="83e7a-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="83e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="83e7a-103">Frissítse a SignalR szolgáltatás hálózati ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="83e7a-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="83e7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83e7a-104">SYNTAX</span></span>

### <span data-ttu-id="83e7a-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83e7a-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83e7a-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83e7a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="83e7a-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e7a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83e7a-108">DESCRIPTION</span></span>
<span data-ttu-id="83e7a-109">Frissítse a SignalR szolgáltatás hálózati ACL-ét, beleértve a nyilvános és privát kapcsolat alapértelmezett műveletét és hálózati ACL-ét.</span><span class="sxs-lookup"><span data-stu-id="83e7a-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="83e7a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83e7a-110">EXAMPLES</span></span>

### <span data-ttu-id="83e7a-111">RESTAPI,ClientConnection engedélyezése nyilvános hálózaton és alapértelmezett művelet elutasítása</span><span class="sxs-lookup"><span data-stu-id="83e7a-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -DefaultAction Deny -PublicNetwork -Allow RESTAPI,ClientConnection

PS C:\>  $networkAcl

DefaultAction PublicNetwork                                        PrivateEndpoints
------------- -------------                                        ----------------
Deny          Microsoft.Azure.Commands.SignalR.Models.PSNetworkAcl {pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1}

PS C:\> $networkAcl.PublicNetwork
Allow                       Deny
-----                       ----
{ClientConnection, RESTAPI} {}
```

### <span data-ttu-id="83e7a-112">Ügyfélkapcsolat és kiszolgálói kapcsolat engedélyezése privát végpontkapcsolat esetén</span><span class="sxs-lookup"><span data-stu-id="83e7a-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="83e7a-113">Ügyfélkapcsolat elutasítása nyilvános hálózat és privát végpontkapcsolat esetén is</span><span class="sxs-lookup"><span data-stu-id="83e7a-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="83e7a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83e7a-114">PARAMETERS</span></span>

### <span data-ttu-id="83e7a-115">-Allow</span><span class="sxs-lookup"><span data-stu-id="83e7a-115">-Allow</span></span>
<span data-ttu-id="83e7a-116">Engedélyezett hálózati ACLs</span><span class="sxs-lookup"><span data-stu-id="83e7a-116">Allowed network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83e7a-117">-AsJob</span></span>
<span data-ttu-id="83e7a-118">Futtassa a parancsmagot a háttérben futó feladatban.</span><span class="sxs-lookup"><span data-stu-id="83e7a-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="83e7a-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="83e7a-119">-DefaultAction</span></span>
<span data-ttu-id="83e7a-120">A SignalR hálózati ACLs alapértelmezett művelete, amely vagy engedélyezi vagy elutasítja.</span><span class="sxs-lookup"><span data-stu-id="83e7a-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="83e7a-121">Eldönti, hogy a hálózati ACL-ek elutasítása vagy a hálózati ACLs engedélyezése hatályba lép-e.</span><span class="sxs-lookup"><span data-stu-id="83e7a-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="83e7a-122">Ha például az alapértelmezett művelet engedélyezett, akkor csak az elutasítási ACLs számít.</span><span class="sxs-lookup"><span data-stu-id="83e7a-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e7a-123">-DefaultProfile</span></span>
<span data-ttu-id="83e7a-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83e7a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e7a-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="83e7a-125">-Deny</span></span>
<span data-ttu-id="83e7a-126">Hálózati ACLs megtagadva</span><span class="sxs-lookup"><span data-stu-id="83e7a-126">Denied network ACLs</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ClientConnection, ServerConnection, RESTAPI

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83e7a-127">-InputObject</span></span>
<span data-ttu-id="83e7a-128">A SignalR erőforrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="83e7a-128">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="83e7a-129">-Name</span></span>
<span data-ttu-id="83e7a-130">A SignalR szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="83e7a-130">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="83e7a-131">-PrivateEndpointName</span></span>
<span data-ttu-id="83e7a-132">A frissíthető magánjellegű végpont(ak) neve</span><span class="sxs-lookup"><span data-stu-id="83e7a-132">Name(s) of private endpoint(s) to be updated</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="83e7a-133">-PublicNetwork</span></span>
<span data-ttu-id="83e7a-134">Nyilvános hálózati ACLs frissítése</span><span class="sxs-lookup"><span data-stu-id="83e7a-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="83e7a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e7a-135">-ResourceGroupName</span></span>
<span data-ttu-id="83e7a-136">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83e7a-136">The resource group name.</span></span>
<span data-ttu-id="83e7a-137">Ha nincs megadva, a program az alapértelmezett beállítást használja.</span><span class="sxs-lookup"><span data-stu-id="83e7a-137">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83e7a-138">-ResourceId</span></span>
<span data-ttu-id="83e7a-139">A SignalR szolgáltatáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83e7a-139">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e7a-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83e7a-140">-Confirm</span></span>
<span data-ttu-id="83e7a-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83e7a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e7a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e7a-142">-WhatIf</span></span>
<span data-ttu-id="83e7a-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83e7a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e7a-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83e7a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e7a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e7a-145">CommonParameters</span></span>
<span data-ttu-id="83e7a-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e7a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e7a-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83e7a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e7a-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83e7a-148">INPUTS</span></span>

### <span data-ttu-id="83e7a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="83e7a-149">System.String</span></span>

## <span data-ttu-id="83e7a-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83e7a-150">OUTPUTS</span></span>

### <span data-ttu-id="83e7a-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="83e7a-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="83e7a-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83e7a-152">NOTES</span></span>

## <span data-ttu-id="83e7a-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83e7a-153">RELATED LINKS</span></span>
