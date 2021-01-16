---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 159b320b24ff1e9ab1b4c71e6c374931ecfeffdd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466242"
---
# <span data-ttu-id="0c203-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c203-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0c203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c203-102">SYNOPSIS</span></span>
<span data-ttu-id="0c203-103">letiltja a magánjellegű végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0c203-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="0c203-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c203-104">SYNTAX</span></span>

### <span data-ttu-id="0c203-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c203-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c203-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="0c203-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
[-PrivateLinkResourceType <string>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c203-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c203-107">DESCRIPTION</span></span>
<span data-ttu-id="0c203-108">Az **Deny-AzPrivateEndpointConnection** parancsmag megtagadja a magánjellegű végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0c203-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="0c203-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c203-109">EXAMPLES</span></span>

### <span data-ttu-id="0c203-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0c203-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="0c203-111">Ez a példa megtagadja a magánjellegű végpontkapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="0c203-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="0c203-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c203-112">PARAMETERS</span></span>

### <span data-ttu-id="0c203-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c203-113">-DefaultProfile</span></span>
<span data-ttu-id="0c203-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c203-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c203-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="0c203-115">-Description</span></span>
<span data-ttu-id="0c203-116">A művelet oka.</span><span class="sxs-lookup"><span data-stu-id="0c203-116">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c203-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0c203-117">-Name</span></span>
<span data-ttu-id="0c203-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0c203-118">The resource name.</span></span>

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

### <span data-ttu-id="0c203-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0c203-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0c203-120">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="0c203-120">The private link resource type.</span></span>

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

### <span data-ttu-id="0c203-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c203-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c203-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0c203-122">The resource group name.</span></span>

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

### <span data-ttu-id="0c203-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c203-123">-ResourceId</span></span>
<span data-ttu-id="0c203-124">A privát végpontkapcsolat Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c203-124">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c203-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c203-125">-ServiceName</span></span>
<span data-ttu-id="0c203-126">Annak a szolgáltatásnak a neve, amelyhez a privát végpontkapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="0c203-126">The name of service that private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="0c203-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c203-127">CommonParameters</span></span>
<span data-ttu-id="0c203-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c203-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c203-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c203-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c203-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c203-130">INPUTS</span></span>

### <span data-ttu-id="0c203-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0c203-131">System.String</span></span>

## <span data-ttu-id="0c203-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c203-132">OUTPUTS</span></span>

### <span data-ttu-id="0c203-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0c203-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="0c203-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c203-134">NOTES</span></span>

## <span data-ttu-id="0c203-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c203-135">RELATED LINKS</span></span>

[<span data-ttu-id="0c203-136">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c203-136">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c203-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c203-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c203-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c203-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c203-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c203-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)