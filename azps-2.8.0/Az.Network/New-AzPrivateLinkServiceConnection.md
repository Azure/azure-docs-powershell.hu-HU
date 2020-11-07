---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 8669eed6e34b2f03d4da8f1f6490a95e4762241d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837926"
---
# <span data-ttu-id="453f4-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="453f4-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="453f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="453f4-102">SYNOPSIS</span></span>
<span data-ttu-id="453f4-103">Létrehoz egy privát kapcsolati szolgáltatás-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="453f4-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="453f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="453f4-104">SYNTAX</span></span>

### <span data-ttu-id="453f4-105">SetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="453f4-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="453f4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="453f4-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="453f4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="453f4-107">DESCRIPTION</span></span>
<span data-ttu-id="453f4-108">**A New-AzPrivateLinkServiceConnection** parancsmag létrehoz egy privát kapcsolati szolgáltatás-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="453f4-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="453f4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="453f4-109">EXAMPLES</span></span>

### <span data-ttu-id="453f4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="453f4-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="453f4-111">Ebben a példában a privát végpont létrehozása című témakörben egy privát kapcsolati szolgáltatás-kapcsolati objektum jön létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="453f4-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="453f4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="453f4-112">PARAMETERS</span></span>

### <span data-ttu-id="453f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453f4-113">-DefaultProfile</span></span>
<span data-ttu-id="453f4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="453f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="453f4-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="453f4-115">-GroupId</span></span>
<span data-ttu-id="453f4-116">A csoport azonosítójának listája.</span><span class="sxs-lookup"><span data-stu-id="453f4-116">The list of group id.</span></span>

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

### <span data-ttu-id="453f4-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="453f4-117">-Name</span></span>
<span data-ttu-id="453f4-118">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="453f4-118">The name of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453f4-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="453f4-119">-PrivateLinkService</span></span>
<span data-ttu-id="453f4-120">A privát hivatkozás szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="453f4-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="453f4-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="453f4-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="453f4-122">A privát hivatkozás szolgáltatás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="453f4-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="453f4-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="453f4-123">-RequestMessage</span></span>
<span data-ttu-id="453f4-124">A kérés üzenete.</span><span class="sxs-lookup"><span data-stu-id="453f4-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="453f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453f4-125">CommonParameters</span></span>
<span data-ttu-id="453f4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="453f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453f4-127">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="453f4-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453f4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="453f4-128">INPUTS</span></span>

### <span data-ttu-id="453f4-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="453f4-129">None</span></span>

## <span data-ttu-id="453f4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="453f4-130">OUTPUTS</span></span>

### <span data-ttu-id="453f4-131">Microsoft. Azure. commands. Network. models. PSPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="453f4-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="453f4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="453f4-132">NOTES</span></span>

## <span data-ttu-id="453f4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="453f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="453f4-134">Új – AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="453f4-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)