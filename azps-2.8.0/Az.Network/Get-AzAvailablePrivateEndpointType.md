---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: a8f256f9a383b3cb7c7aed014474c1ea24706106
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837360"
---
# <span data-ttu-id="d63c0-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d63c0-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="d63c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d63c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d63c0-103">A rendelkezésre álló privát végpontok típusának visszaadása a helyen</span><span class="sxs-lookup"><span data-stu-id="d63c0-103">Return available private end point types in the location</span></span>

## <span data-ttu-id="d63c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d63c0-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d63c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d63c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d63c0-106">A **Get-AzAvailablePrivateEndpointType** parancsmag az összes elérhető privát végpont-típust visszaállítja a helyről.</span><span class="sxs-lookup"><span data-stu-id="d63c0-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="d63c0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d63c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d63c0-108">Például</span><span class="sxs-lookup"><span data-stu-id="d63c0-108">Example</span></span>
```
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsot.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="d63c0-109">Ez a példa a hely minden elérhető privát végpont-típusát visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="d63c0-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="d63c0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d63c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d63c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d63c0-111">-DefaultProfile</span></span>
<span data-ttu-id="d63c0-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d63c0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d63c0-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d63c0-113">-Location</span></span>
<span data-ttu-id="d63c0-114">A hely.</span><span class="sxs-lookup"><span data-stu-id="d63c0-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d63c0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d63c0-115">-ResourceGroupName</span></span>
<span data-ttu-id="d63c0-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="d63c0-116">The resource group name.</span></span>

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

### <span data-ttu-id="d63c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d63c0-117">CommonParameters</span></span>
<span data-ttu-id="d63c0-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d63c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d63c0-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d63c0-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d63c0-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d63c0-120">INPUTS</span></span>

### <span data-ttu-id="d63c0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d63c0-121">System.String</span></span>

## <span data-ttu-id="d63c0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d63c0-122">OUTPUTS</span></span>

### <span data-ttu-id="d63c0-123">Microsoft. Azure. commands. Network. models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="d63c0-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="d63c0-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d63c0-124">NOTES</span></span>

## <span data-ttu-id="d63c0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d63c0-125">RELATED LINKS</span></span>
