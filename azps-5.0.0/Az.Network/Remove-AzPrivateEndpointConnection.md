---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188106"
---
# <span data-ttu-id="99d35-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="99d35-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="99d35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99d35-102">SYNOPSIS</span></span>
<span data-ttu-id="99d35-103">Privát végpont-kapcsolat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="99d35-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="99d35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99d35-104">SYNTAX</span></span>

### <span data-ttu-id="99d35-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99d35-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99d35-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="99d35-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d35-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99d35-107">DESCRIPTION</span></span>
<span data-ttu-id="99d35-108">A **Remove-AzPrivateEndpointConnection** parancsmag a privát végpontok közötti kapcsolatot távolítja el.</span><span class="sxs-lookup"><span data-stu-id="99d35-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="99d35-109">Példák</span><span class="sxs-lookup"><span data-stu-id="99d35-109">EXAMPLES</span></span>

### <span data-ttu-id="99d35-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="99d35-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="99d35-111">Ebben a példában a MyPrivateEndpointConnection1 nevű privát végpont-kapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="99d35-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="99d35-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99d35-112">PARAMETERS</span></span>

### <span data-ttu-id="99d35-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99d35-113">-AsJob</span></span>
<span data-ttu-id="99d35-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99d35-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99d35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d35-115">-DefaultProfile</span></span>
<span data-ttu-id="99d35-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99d35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d35-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99d35-117">-Force</span></span>
<span data-ttu-id="99d35-118">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="99d35-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="99d35-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="99d35-119">-Name</span></span>
<span data-ttu-id="99d35-120">A privát végpont-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="99d35-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d35-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99d35-121">-PassThru</span></span>
<span data-ttu-id="99d35-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="99d35-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99d35-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="99d35-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99d35-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="99d35-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="99d35-125">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="99d35-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d35-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d35-126">-ResourceGroupName</span></span>
<span data-ttu-id="99d35-127">A privát végpont-kapcsolat erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="99d35-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d35-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99d35-128">-ResourceId</span></span>
<span data-ttu-id="99d35-129">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="99d35-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d35-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="99d35-130">-ServiceName</span></span>
<span data-ttu-id="99d35-131">Annak a szolgáltatásnak a neve, amelyhez a privát végpont-kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="99d35-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d35-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99d35-132">-Confirm</span></span>
<span data-ttu-id="99d35-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99d35-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d35-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d35-134">-WhatIf</span></span>
<span data-ttu-id="99d35-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99d35-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d35-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99d35-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d35-137">CommonParameters</span></span>
<span data-ttu-id="99d35-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99d35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d35-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="99d35-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d35-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d35-140">INPUTS</span></span>

### <span data-ttu-id="99d35-141">System. String</span><span class="sxs-lookup"><span data-stu-id="99d35-141">System.String</span></span>

## <span data-ttu-id="99d35-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d35-142">OUTPUTS</span></span>

### <span data-ttu-id="99d35-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99d35-143">System.Boolean</span></span>

## <span data-ttu-id="99d35-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99d35-144">NOTES</span></span>

## <span data-ttu-id="99d35-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99d35-145">RELATED LINKS</span></span>

[<span data-ttu-id="99d35-146">Jóváhagyás – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="99d35-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="99d35-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="99d35-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="99d35-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="99d35-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="99d35-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="99d35-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
