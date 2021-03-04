---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924922"
---
# <span data-ttu-id="c18b8-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="c18b8-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="c18b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c18b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c18b8-103">Minden olyan érvényes kódot bevesz, amelybe ez az IotHub át tud áttűnni.</span><span class="sxs-lookup"><span data-stu-id="c18b8-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="c18b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c18b8-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c18b8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c18b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c18b8-106">Beveszi az összes olyan érvényes kódot, amelybe ez az IotHub át tud áttűnni.</span><span class="sxs-lookup"><span data-stu-id="c18b8-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="c18b8-107">Az IotHub nem tud áttűnni a szabad és a fizetős skus között, és fordítva.</span><span class="sxs-lookup"><span data-stu-id="c18b8-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="c18b8-108">Ehhez törölnie és újból létre kell hoznia az iothubot.</span><span class="sxs-lookup"><span data-stu-id="c18b8-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="c18b8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c18b8-109">EXAMPLES</span></span>

### <span data-ttu-id="c18b8-110">1. példa Az érvényes skus lekérte</span><span class="sxs-lookup"><span data-stu-id="c18b8-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c18b8-111">A "myiothub" nevű IotHub összes skusját tartalmazza</span><span class="sxs-lookup"><span data-stu-id="c18b8-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c18b8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c18b8-112">PARAMETERS</span></span>

### <span data-ttu-id="c18b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18b8-113">-DefaultProfile</span></span>
<span data-ttu-id="c18b8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c18b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c18b8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c18b8-115">-Name</span></span>
<span data-ttu-id="c18b8-116">Az IoT-központ neve.</span><span class="sxs-lookup"><span data-stu-id="c18b8-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c18b8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c18b8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c18b8-118">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c18b8-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c18b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18b8-119">CommonParameters</span></span>
<span data-ttu-id="c18b8-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c18b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18b8-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c18b8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18b8-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c18b8-122">INPUTS</span></span>

### <span data-ttu-id="c18b8-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c18b8-123">System.String</span></span>

## <span data-ttu-id="c18b8-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c18b8-124">OUTPUTS</span></span>

### <span data-ttu-id="c18b8-125">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="c18b8-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="c18b8-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c18b8-126">NOTES</span></span>

## <span data-ttu-id="c18b8-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c18b8-127">RELATED LINKS</span></span>
