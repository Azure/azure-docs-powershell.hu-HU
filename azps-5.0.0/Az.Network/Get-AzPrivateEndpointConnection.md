---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302021"
---
# <span data-ttu-id="25cef-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25cef-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="25cef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25cef-102">SYNOPSIS</span></span>
<span data-ttu-id="25cef-103">Privát végpont-kapcsolati erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="25cef-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="25cef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25cef-104">SYNTAX</span></span>

### <span data-ttu-id="25cef-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25cef-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25cef-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25cef-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="25cef-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="25cef-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="25cef-108">DESCRIPTION</span></span>
<span data-ttu-id="25cef-109">A **Get-AzPrivateEndpointConnection** parancsmag egy privát végpont-kapcsolati erőforrást keres.</span><span class="sxs-lookup"><span data-stu-id="25cef-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="25cef-110">Példák</span><span class="sxs-lookup"><span data-stu-id="25cef-110">EXAMPLES</span></span>

### <span data-ttu-id="25cef-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25cef-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="25cef-112">Ez a példa az összes privát végpont-kapcsolat listáját adja vissza a MySQL nevű SQL Serverhez.</span><span class="sxs-lookup"><span data-stu-id="25cef-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="25cef-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="25cef-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="25cef-114">Ebben a példában a MyPrivateEndpointConnection1 nevű privát végponti kapcsolat tartozik a MyPrivateLinkService nevű privát hivatkozás szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="25cef-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="25cef-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25cef-115">PARAMETERS</span></span>

### <span data-ttu-id="25cef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cef-116">-DefaultProfile</span></span>
<span data-ttu-id="25cef-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25cef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cef-118">-Leírás</span><span class="sxs-lookup"><span data-stu-id="25cef-118">-Description</span></span>
<span data-ttu-id="25cef-119">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="25cef-119">The reason of action.</span></span>

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

### <span data-ttu-id="25cef-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25cef-120">-Name</span></span>
<span data-ttu-id="25cef-121">A privát végpont-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="25cef-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25cef-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="25cef-123">A privát végpont-kapcsolatot tartalmazó "privát kapcsolat" erőforrás Azure Resource Manager azonosítója.</span><span class="sxs-lookup"><span data-stu-id="25cef-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="25cef-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="25cef-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="25cef-125">A magánjellegű kapcsolat erőforrástípus.</span><span class="sxs-lookup"><span data-stu-id="25cef-125">The private link resource type.</span></span>

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

### <span data-ttu-id="25cef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25cef-126">-ResourceGroupName</span></span>
<span data-ttu-id="25cef-127">A privát végpont-kapcsolat erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="25cef-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25cef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25cef-128">-ResourceId</span></span>
<span data-ttu-id="25cef-129">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="25cef-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25cef-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="25cef-130">-ServiceName</span></span>
<span data-ttu-id="25cef-131">Annak a szolgáltatásnak a neve, amelyhez a privát végpont-kapcsolat tartozik.</span><span class="sxs-lookup"><span data-stu-id="25cef-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="25cef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cef-132">CommonParameters</span></span>
<span data-ttu-id="25cef-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25cef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cef-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25cef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cef-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25cef-135">INPUTS</span></span>

### <span data-ttu-id="25cef-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25cef-136">System.String</span></span>

## <span data-ttu-id="25cef-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25cef-137">OUTPUTS</span></span>

### <span data-ttu-id="25cef-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25cef-138">System.Boolean</span></span>

## <span data-ttu-id="25cef-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25cef-139">NOTES</span></span>

## <span data-ttu-id="25cef-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25cef-140">RELATED LINKS</span></span>

[<span data-ttu-id="25cef-141">Jóváhagyás – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25cef-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="25cef-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25cef-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="25cef-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25cef-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="25cef-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25cef-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
