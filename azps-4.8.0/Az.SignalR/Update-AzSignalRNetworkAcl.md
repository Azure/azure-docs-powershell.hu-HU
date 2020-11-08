---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalrnetworkacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalRNetworkAcl.md
ms.openlocfilehash: afe9e1f604754c88035ed79f0eb480321ca348ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025974"
---
# <span data-ttu-id="77c9f-101">Update-AzSignalRNetworkAcl</span><span class="sxs-lookup"><span data-stu-id="77c9f-101">Update-AzSignalRNetworkAcl</span></span>

## <span data-ttu-id="77c9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="77c9f-103">A Szignálók hálózati hozzáférés-vezérlési szolgáltatásának frissítése</span><span class="sxs-lookup"><span data-stu-id="77c9f-103">Update the Network ACL of a SignalR service.</span></span>

## <span data-ttu-id="77c9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77c9f-104">SYNTAX</span></span>

### <span data-ttu-id="77c9f-105">ResourceGroupParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77c9f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalRNetworkAcl [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-DefaultAction <String>]
 [-PublicNetwork] [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77c9f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77c9f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -ResourceId <String> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77c9f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77c9f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalRNetworkAcl -InputObject <PSSignalRResource> [-AsJob] [-DefaultAction <String>] [-PublicNetwork]
 [-PrivateEndpointName <String[]>] [-Allow <String[]>] [-Deny <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77c9f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="77c9f-108">DESCRIPTION</span></span>
<span data-ttu-id="77c9f-109">Frissítse a Szignálók hálózati hozzáférés-vezérlési szolgáltatását, például az alapértelmezett műveleteket és a hálózat hozzáférési szabálygyűjteményeit a nyilvános és a privát kapcsolathoz.</span><span class="sxs-lookup"><span data-stu-id="77c9f-109">Update the Network ACL of a SignalR service, including the default action and the network Acls for public and private connection.</span></span>

## <span data-ttu-id="77c9f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="77c9f-110">EXAMPLES</span></span>

### <span data-ttu-id="77c9f-111">A RESTAPI engedélyezése, a nyilvános hálózat ClientConnection és az alapértelmezett műveletek megtagadásának beállítása</span><span class="sxs-lookup"><span data-stu-id="77c9f-111">Allow RESTAPI,ClientConnection for public network and set default action to Deny</span></span>
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

### <span data-ttu-id="77c9f-112">Ügyfél-kapcsolat és kiszolgáló kapcsolat engedélyezése privát végpontos kapcsolat esetén</span><span class="sxs-lookup"><span data-stu-id="77c9f-112">Allow client connection and server connection for a private endpoint connection</span></span>
```powershell
PS C:\> $networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -Allow ClientConnection,ServerConnection

PS C:\>$networkAcl.PrivateEndpoints[0]

Name                                           Allow                                Deny
----                                           -----                                ----
pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1 {ServerConnection, ClientConnection} {}
```

### <span data-ttu-id="77c9f-113">Ügyfél-kapcsolat elutasítása nyilvános hálózat és privát végpontos kapcsolat esetén</span><span class="sxs-lookup"><span data-stu-id="77c9f-113">Deny client connection for both public network and a private endpoint connection</span></span>
```powershell
PS C:\>$networkAcl = Update-AzSignalRNetworkAcl -Name pssignalr -ResourceGroupName test_resource_group -PrivateEndpointName pssignalr.70197ffc-d138-49a5-a336-98b21a8d04d1  -PublicNetwork -Deny ClientConnection
```

## <span data-ttu-id="77c9f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77c9f-114">PARAMETERS</span></span>

### <span data-ttu-id="77c9f-115">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="77c9f-115">-Allow</span></span>
<span data-ttu-id="77c9f-116">Engedélyezett hálózati ACL-eket</span><span class="sxs-lookup"><span data-stu-id="77c9f-116">Allowed network ACLs</span></span>

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

### <span data-ttu-id="77c9f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77c9f-117">-AsJob</span></span>
<span data-ttu-id="77c9f-118">Futtassa a parancsmagot a háttérben.</span><span class="sxs-lookup"><span data-stu-id="77c9f-118">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="77c9f-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="77c9f-119">-DefaultAction</span></span>
<span data-ttu-id="77c9f-120">A jelzést tartalmazó hálózat ACL-je alapértelmezett működésének engedélyezése vagy elutasítása.</span><span class="sxs-lookup"><span data-stu-id="77c9f-120">Default Action of SignalR network ACLs, either allow or deny.</span></span> <span data-ttu-id="77c9f-121">Ez a beállítás azt határozza meg, hogy a hálózati hozzáférés-vezérlési listák megtagadása vagy a hálózati ACL-</span><span class="sxs-lookup"><span data-stu-id="77c9f-121">It decides whether deny network ACLs or allow network ACLs take effect.</span></span> <span data-ttu-id="77c9f-122">Ha például az alapértelmezett művelet engedélyezve van, akkor csak az ACL-eket kell megtagadnia.</span><span class="sxs-lookup"><span data-stu-id="77c9f-122">For example, if the default action is allow, then only the deny ACLs matters.</span></span>

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

### <span data-ttu-id="77c9f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c9f-123">-DefaultProfile</span></span>
<span data-ttu-id="77c9f-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77c9f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c9f-125">-Deny</span><span class="sxs-lookup"><span data-stu-id="77c9f-125">-Deny</span></span>
<span data-ttu-id="77c9f-126">A hálózat hozzáférési szabálygyűjteményeit megtagadva</span><span class="sxs-lookup"><span data-stu-id="77c9f-126">Denied network ACLs</span></span>

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

### <span data-ttu-id="77c9f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77c9f-127">-InputObject</span></span>
<span data-ttu-id="77c9f-128">A jelző erőforrás-objektum.</span><span class="sxs-lookup"><span data-stu-id="77c9f-128">The SignalR resource object.</span></span>

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

### <span data-ttu-id="77c9f-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77c9f-129">-Name</span></span>
<span data-ttu-id="77c9f-130">A szignáló szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="77c9f-130">The SignalR service name.</span></span>

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

### <span data-ttu-id="77c9f-131">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="77c9f-131">-PrivateEndpointName</span></span>
<span data-ttu-id="77c9f-132">A frissítendő magánjellegű végpontok neve (i)</span><span class="sxs-lookup"><span data-stu-id="77c9f-132">Name(s) of private endpoint(s) to be updated</span></span>

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

### <span data-ttu-id="77c9f-133">-PublicNetwork</span><span class="sxs-lookup"><span data-stu-id="77c9f-133">-PublicNetwork</span></span>
<span data-ttu-id="77c9f-134">Nyilvános hálózati hozzáférés-vezérlési listák frissítése</span><span class="sxs-lookup"><span data-stu-id="77c9f-134">Update public network ACLs</span></span>

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

### <span data-ttu-id="77c9f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c9f-135">-ResourceGroupName</span></span>
<span data-ttu-id="77c9f-136">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="77c9f-136">The resource group name.</span></span>
<span data-ttu-id="77c9f-137">A program az alapértelmezett értéket használja, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="77c9f-137">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="77c9f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77c9f-138">-ResourceId</span></span>
<span data-ttu-id="77c9f-139">A Szignál Szolgáltató erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77c9f-139">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="77c9f-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77c9f-140">-Confirm</span></span>
<span data-ttu-id="77c9f-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77c9f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77c9f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77c9f-142">-WhatIf</span></span>
<span data-ttu-id="77c9f-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77c9f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77c9f-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77c9f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77c9f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c9f-145">CommonParameters</span></span>
<span data-ttu-id="77c9f-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77c9f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c9f-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77c9f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c9f-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c9f-148">INPUTS</span></span>

### <span data-ttu-id="77c9f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="77c9f-149">System.String</span></span>

## <span data-ttu-id="77c9f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77c9f-150">OUTPUTS</span></span>

### <span data-ttu-id="77c9f-151">Microsoft. Azure. Command. Signal. models. PSSignalRNetworkAcls</span><span class="sxs-lookup"><span data-stu-id="77c9f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRNetworkAcls</span></span>

## <span data-ttu-id="77c9f-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77c9f-152">NOTES</span></span>

## <span data-ttu-id="77c9f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77c9f-153">RELATED LINKS</span></span>
