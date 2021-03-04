---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: d2df4f7f5ed073d357daa1113a8e0c7477a05cce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919722"
---
# <span data-ttu-id="7f287-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7f287-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7f287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f287-102">SYNOPSIS</span></span>
<span data-ttu-id="7f287-103">Egy privát végpontkapcsolat-erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="7f287-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="7f287-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f287-104">SYNTAX</span></span>

### <span data-ttu-id="7f287-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f287-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f287-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7f287-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f287-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="7f287-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f287-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f287-108">DESCRIPTION</span></span>
<span data-ttu-id="7f287-109">A **Get-AzPrivateEndpointConnection** parancsmag lekér egy privát végpontkapcsolat-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7f287-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="7f287-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f287-110">EXAMPLES</span></span>

### <span data-ttu-id="7f287-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7f287-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="7f287-112">Ebben a példában a Mysql nevű sql Server összes privát végpontkapcsolatának listáját adhatja vissza.</span><span class="sxs-lookup"><span data-stu-id="7f287-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="7f287-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7f287-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="7f287-114">Ebben a példában egy MyPrivateEndpointConnection1 nevű privát végpontkapcsolat tartozik a MyPrivateLinkService nevű privát hivatkozásszolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="7f287-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="7f287-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f287-115">PARAMETERS</span></span>

### <span data-ttu-id="7f287-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f287-116">-DefaultProfile</span></span>
<span data-ttu-id="7f287-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f287-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f287-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7f287-118">-Description</span></span>
<span data-ttu-id="7f287-119">A művelet oka.</span><span class="sxs-lookup"><span data-stu-id="7f287-119">The reason of action.</span></span>

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

### <span data-ttu-id="7f287-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7f287-120">-Name</span></span>
<span data-ttu-id="7f287-121">A privát végpontkapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="7f287-121">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f287-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7f287-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7f287-123">Annak a privát hivatkozás-erőforrásnak az Azure-erőforrás-azonosítója, amelyhez a privát végpontkapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="7f287-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f287-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7f287-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7f287-125">A privát csatolás erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="7f287-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f287-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f287-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f287-127">A magánjellegű végpontkapcsolat erőforráscsoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="7f287-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7f287-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f287-128">-ResourceId</span></span>
<span data-ttu-id="7f287-129">A privát végpontkapcsolat Azure-erőforrás-kezelői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7f287-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7f287-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7f287-130">-ServiceName</span></span>
<span data-ttu-id="7f287-131">Annak a szolgáltatásnak a neve, amelyhez a privát végpontkapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="7f287-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="7f287-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f287-132">CommonParameters</span></span>
<span data-ttu-id="7f287-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f287-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f287-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f287-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f287-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f287-135">INPUTS</span></span>

### <span data-ttu-id="7f287-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7f287-136">System.String</span></span>

## <span data-ttu-id="7f287-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f287-137">OUTPUTS</span></span>

### <span data-ttu-id="7f287-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f287-138">System.Boolean</span></span>

## <span data-ttu-id="7f287-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f287-139">NOTES</span></span>

## <span data-ttu-id="7f287-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f287-140">RELATED LINKS</span></span>

[<span data-ttu-id="7f287-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7f287-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7f287-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7f287-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7f287-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7f287-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7f287-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7f287-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
