---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: 49fad6adf339afb9dacd6f916cf0abb8e6bb3728
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837361"
---
# <span data-ttu-id="9502d-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9502d-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="9502d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9502d-102">SYNOPSIS</span></span>
<span data-ttu-id="9502d-103">A magánhálózati szolgáltatás-azonosítók egy olyan sorát kapja, amely egy privát végponthoz kapcsolható az automatikus jóváhagyással.</span><span class="sxs-lookup"><span data-stu-id="9502d-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="9502d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9502d-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9502d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9502d-105">DESCRIPTION</span></span>
<span data-ttu-id="9502d-106">A **Get-AzAutoApprovedPrivateLinkService** a magánhálózati szolgáltatás-azonosítók egy olyan sorát kapja, amely egy privát végponthoz kapcsolható az automatikus jóváhagyással.</span><span class="sxs-lookup"><span data-stu-id="9502d-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="9502d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9502d-107">EXAMPLES</span></span>

### <span data-ttu-id="9502d-108">Például</span><span class="sxs-lookup"><span data-stu-id="9502d-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="9502d-109">Ez a példa a privát hivatkozás szolgáltatás-azonosító egy olyan sorát adja eredményül, amely egy privát végponthoz kapcsolható az automatikus jóváhagyással.</span><span class="sxs-lookup"><span data-stu-id="9502d-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="9502d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9502d-110">PARAMETERS</span></span>

### <span data-ttu-id="9502d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9502d-111">-DefaultProfile</span></span>
<span data-ttu-id="9502d-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9502d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9502d-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="9502d-113">-Location</span></span>
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

### <span data-ttu-id="9502d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9502d-114">-ResourceGroupName</span></span>
<span data-ttu-id="9502d-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9502d-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9502d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9502d-116">CommonParameters</span></span>
<span data-ttu-id="9502d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9502d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9502d-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9502d-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9502d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9502d-119">INPUTS</span></span>

### <span data-ttu-id="9502d-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="9502d-120">None</span></span>

## <span data-ttu-id="9502d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9502d-121">OUTPUTS</span></span>

### <span data-ttu-id="9502d-122">Microsoft. Azure. commands. Network. models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="9502d-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="9502d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9502d-123">NOTES</span></span>

## <span data-ttu-id="9502d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9502d-124">RELATED LINKS</span></span>
