---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmDnsAvailability.md
ms.openlocfilehash: 348fd7e97566520b27163de91d4d52162d4c3978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498268"
---
# <span data-ttu-id="ab4c7-101">Test-AzureRmDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="ab4c7-101">Test-AzureRmDnsAvailability</span></span>

## <span data-ttu-id="ab4c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab4c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4c7-103">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="ab4c7-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab4c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab4c7-104">SYNTAX</span></span>

```
Test-AzureRmDnsAvailability -DomainNameLabel <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab4c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab4c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4c7-106">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="ab4c7-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="ab4c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab4c7-107">EXAMPLES</span></span>

### <span data-ttu-id="ab4c7-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="ab4c7-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzureRmDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="ab4c7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab4c7-109">PARAMETERS</span></span>

### <span data-ttu-id="ab4c7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4c7-110">-DefaultProfile</span></span>
<span data-ttu-id="ab4c7-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ab4c7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4c7-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ab4c7-112">-DomainNameLabel</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainQualifiedName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4c7-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="ab4c7-113">-Location</span></span>
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

### <span data-ttu-id="ab4c7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4c7-114">CommonParameters</span></span>
<span data-ttu-id="ab4c7-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab4c7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4c7-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4c7-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4c7-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab4c7-117">INPUTS</span></span>

### <span data-ttu-id="ab4c7-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab4c7-118">None</span></span>

## <span data-ttu-id="ab4c7-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab4c7-119">OUTPUTS</span></span>

### <span data-ttu-id="ab4c7-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab4c7-120">System.Boolean</span></span>

## <span data-ttu-id="ab4c7-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab4c7-121">NOTES</span></span>

## <span data-ttu-id="ab4c7-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab4c7-122">RELATED LINKS</span></span>
