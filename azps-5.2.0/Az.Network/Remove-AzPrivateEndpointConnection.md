---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350201"
---
# <span data-ttu-id="4854e-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4854e-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="4854e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4854e-102">SYNOPSIS</span></span>
<span data-ttu-id="4854e-103">Eltávolít egy privát végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4854e-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="4854e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4854e-104">SYNTAX</span></span>

### <span data-ttu-id="4854e-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4854e-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4854e-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="4854e-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4854e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4854e-107">DESCRIPTION</span></span>
<span data-ttu-id="4854e-108">A **Remove-AzPrivateEndpointConnection** parancsmag eltávolítja a magánjellegű végpontkapcsolatokat.</span><span class="sxs-lookup"><span data-stu-id="4854e-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="4854e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4854e-109">EXAMPLES</span></span>

### <span data-ttu-id="4854e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4854e-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="4854e-111">Ebben a példában eltávolítunk egy MyPrivateEndpointConnection1 nevű privát végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="4854e-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="4854e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4854e-112">PARAMETERS</span></span>

### <span data-ttu-id="4854e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4854e-113">-AsJob</span></span>
<span data-ttu-id="4854e-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4854e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4854e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4854e-115">-DefaultProfile</span></span>
<span data-ttu-id="4854e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4854e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4854e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4854e-117">-Force</span></span>
<span data-ttu-id="4854e-118">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="4854e-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="4854e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4854e-119">-Name</span></span>
<span data-ttu-id="4854e-120">A privát végpontkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="4854e-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4854e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4854e-121">-PassThru</span></span>
<span data-ttu-id="4854e-122">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="4854e-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4854e-123">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4854e-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4854e-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="4854e-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="4854e-125">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="4854e-125">The private link resource type.</span></span>

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

### <span data-ttu-id="4854e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4854e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4854e-127">A magánjellegű végpontkapcsolat erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="4854e-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4854e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4854e-128">-ResourceId</span></span>
<span data-ttu-id="4854e-129">A privát végpontkapcsolat Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4854e-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="4854e-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4854e-130">-ServiceName</span></span>
<span data-ttu-id="4854e-131">Annak a szolgáltatásnak a neve, amelyhez a privát végpontkapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="4854e-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="4854e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4854e-132">-Confirm</span></span>
<span data-ttu-id="4854e-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4854e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4854e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4854e-134">-WhatIf</span></span>
<span data-ttu-id="4854e-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4854e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4854e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4854e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4854e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4854e-137">CommonParameters</span></span>
<span data-ttu-id="4854e-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4854e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4854e-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4854e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4854e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4854e-140">INPUTS</span></span>

### <span data-ttu-id="4854e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4854e-141">System.String</span></span>

## <span data-ttu-id="4854e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4854e-142">OUTPUTS</span></span>

### <span data-ttu-id="4854e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4854e-143">System.Boolean</span></span>

## <span data-ttu-id="4854e-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4854e-144">NOTES</span></span>

## <span data-ttu-id="4854e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4854e-145">RELATED LINKS</span></span>

[<span data-ttu-id="4854e-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4854e-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4854e-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4854e-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4854e-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4854e-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="4854e-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="4854e-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
