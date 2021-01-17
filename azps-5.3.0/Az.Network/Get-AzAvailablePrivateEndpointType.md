---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467378"
---
# <span data-ttu-id="696cf-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="696cf-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="696cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696cf-102">SYNOPSIS</span></span>
<span data-ttu-id="696cf-103">A hely rendelkezésre álló személyes végponttípusokat ad vissza.</span><span class="sxs-lookup"><span data-stu-id="696cf-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="696cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="696cf-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696cf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="696cf-105">DESCRIPTION</span></span>
<span data-ttu-id="696cf-106">A **Get-AzAvailablePrivateEndpointType** parancsmag visszaadja a hely összes elérhető személyes végponttípusát.</span><span class="sxs-lookup"><span data-stu-id="696cf-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="696cf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="696cf-107">EXAMPLES</span></span>

### <span data-ttu-id="696cf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="696cf-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="696cf-109">Ez a példa a hely összes elérhető személyes végponttípusát visszaadja.</span><span class="sxs-lookup"><span data-stu-id="696cf-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="696cf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696cf-110">PARAMETERS</span></span>

### <span data-ttu-id="696cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696cf-111">-DefaultProfile</span></span>
<span data-ttu-id="696cf-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="696cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696cf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="696cf-113">-Location</span></span>
<span data-ttu-id="696cf-114">A hely.</span><span class="sxs-lookup"><span data-stu-id="696cf-114">The location.</span></span>

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

### <span data-ttu-id="696cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="696cf-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="696cf-116">The resource group name.</span></span>

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

### <span data-ttu-id="696cf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696cf-117">CommonParameters</span></span>
<span data-ttu-id="696cf-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696cf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696cf-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="696cf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696cf-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="696cf-120">INPUTS</span></span>

### <span data-ttu-id="696cf-121">System.String</span><span class="sxs-lookup"><span data-stu-id="696cf-121">System.String</span></span>

## <span data-ttu-id="696cf-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="696cf-122">OUTPUTS</span></span>

### <span data-ttu-id="696cf-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="696cf-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="696cf-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="696cf-124">NOTES</span></span>

## <span data-ttu-id="696cf-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="696cf-125">RELATED LINKS</span></span>
