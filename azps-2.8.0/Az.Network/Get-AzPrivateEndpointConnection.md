---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837296"
---
# <span data-ttu-id="25763-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25763-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="25763-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25763-102">SYNOPSIS</span></span>
<span data-ttu-id="25763-103">Privát végpont-kapcsolati erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="25763-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="25763-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25763-104">SYNTAX</span></span>

### <span data-ttu-id="25763-105">ByResourceId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="25763-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25763-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="25763-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25763-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="25763-107">DESCRIPTION</span></span>
<span data-ttu-id="25763-108">A **Get-AzPrivateEndpointConnection** parancsmag egy privát végpont-kapcsolati erőforrást keres.</span><span class="sxs-lookup"><span data-stu-id="25763-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="25763-109">Példák</span><span class="sxs-lookup"><span data-stu-id="25763-109">EXAMPLES</span></span>

### <span data-ttu-id="25763-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25763-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="25763-111">Ebben a példában a MyPrivateEndpointConnection1 nevű privát végponti kapcsolat jelenik meg</span><span class="sxs-lookup"><span data-stu-id="25763-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="25763-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25763-112">PARAMETERS</span></span>

### <span data-ttu-id="25763-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25763-113">-DefaultProfile</span></span>
<span data-ttu-id="25763-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25763-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25763-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="25763-115">-Description</span></span>
<span data-ttu-id="25763-116">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="25763-116">The reason of action.</span></span>

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

### <span data-ttu-id="25763-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25763-117">-Name</span></span>
<span data-ttu-id="25763-118">A privát végpont-kapcsolat neve.</span><span class="sxs-lookup"><span data-stu-id="25763-118">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25763-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25763-119">-ResourceGroupName</span></span>
<span data-ttu-id="25763-120">A privát végpont-kapcsolat erőforráscsoport-neve.</span><span class="sxs-lookup"><span data-stu-id="25763-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25763-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25763-121">-ResourceId</span></span>
<span data-ttu-id="25763-122">A privát végpont-kapcsolat Azure Resource Manager azonosítója</span><span class="sxs-lookup"><span data-stu-id="25763-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="25763-123">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="25763-123">-ServiceName</span></span>
<span data-ttu-id="25763-124">A privát végpont-kapcsolatot tartalmazó privát kapcsolat szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="25763-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="25763-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25763-125">CommonParameters</span></span>
<span data-ttu-id="25763-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25763-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25763-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="25763-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25763-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25763-128">INPUTS</span></span>

### <span data-ttu-id="25763-129">System. String</span><span class="sxs-lookup"><span data-stu-id="25763-129">System.String</span></span>

## <span data-ttu-id="25763-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25763-130">OUTPUTS</span></span>

### <span data-ttu-id="25763-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25763-131">System.Boolean</span></span>

## <span data-ttu-id="25763-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25763-132">NOTES</span></span>

## <span data-ttu-id="25763-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25763-133">RELATED LINKS</span></span>

[<span data-ttu-id="25763-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="25763-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
