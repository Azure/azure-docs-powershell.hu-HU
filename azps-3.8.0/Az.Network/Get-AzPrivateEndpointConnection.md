---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013308"
---
# <span data-ttu-id="5be29-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5be29-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="5be29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5be29-102">SYNOPSIS</span></span>
<span data-ttu-id="5be29-103">Privát végpont-kapcsolati erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="5be29-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="5be29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5be29-104">SYNTAX</span></span>

### <span data-ttu-id="5be29-105">ByPrivateLinkResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5be29-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be29-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5be29-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5be29-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="5be29-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be29-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5be29-108">DESCRIPTION</span></span>
<span data-ttu-id="5be29-109">A **Get-AzPrivateEndpointConnection** parancsmag egy privát végpont-kapcsolati erőforrást keres.</span><span class="sxs-lookup"><span data-stu-id="5be29-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="5be29-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5be29-110">EXAMPLES</span></span>

### <span data-ttu-id="5be29-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5be29-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="5be29-112">Ez a példa az összes privát végpont-kapcsolat listáját adja vissza a MySQL nevű SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="5be29-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="5be29-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="5be29-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="5be29-114">Ebben a példában a MyPrivateEndpointConnection1 nevű privát végponti kapcsolat tartozik a MyPrivateLinkService nevű privát hivatkozás szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="5be29-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="5be29-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5be29-115">PARAMETERS</span></span>

### <span data-ttu-id="5be29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be29-116">-DefaultProfile</span></span>
<span data-ttu-id="5be29-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5be29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5be29-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5be29-118">-Name</span></span>
<span data-ttu-id="5be29-119">A privát végpont-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="5be29-119">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="5be29-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="5be29-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5be29-121">A privát végpont-kapcsolatot tartalmazó "privát kapcsolat" erőforrás Azure Resource Manager azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5be29-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="5be29-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="5be29-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="5be29-123">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="5be29-123">The private link resource type.</span></span>

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

### <span data-ttu-id="5be29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be29-124">-ResourceGroupName</span></span>
<span data-ttu-id="5be29-125">A privát végpont-kapcsolat erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="5be29-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="5be29-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5be29-126">-ResourceId</span></span>
<span data-ttu-id="5be29-127">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="5be29-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="5be29-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="5be29-128">-ServiceName</span></span>
<span data-ttu-id="5be29-129">Annak a szolgáltatásnak a neve, amelyhez a privát végpont-kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="5be29-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="5be29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be29-130">CommonParameters</span></span>
<span data-ttu-id="5be29-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5be29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be29-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5be29-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be29-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be29-133">INPUTS</span></span>

### <span data-ttu-id="5be29-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5be29-134">System.String</span></span>

## <span data-ttu-id="5be29-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5be29-135">OUTPUTS</span></span>

### <span data-ttu-id="5be29-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5be29-136">System.Boolean</span></span>

## <span data-ttu-id="5be29-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5be29-137">NOTES</span></span>

## <span data-ttu-id="5be29-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5be29-138">RELATED LINKS</span></span>

[<span data-ttu-id="5be29-139">Jóváhagyás – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5be29-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5be29-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5be29-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5be29-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5be29-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="5be29-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5be29-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
