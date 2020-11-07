---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 6d6626164000957ffaa987a71131987f35a977c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669936"
---
# <span data-ttu-id="e719b-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="e719b-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="e719b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e719b-102">SYNOPSIS</span></span>
<span data-ttu-id="e719b-103">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="e719b-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="e719b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e719b-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e719b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e719b-105">DESCRIPTION</span></span>
<span data-ttu-id="e719b-106">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="e719b-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="e719b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e719b-107">EXAMPLES</span></span>

### <span data-ttu-id="e719b-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="e719b-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="e719b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e719b-109">PARAMETERS</span></span>

### <span data-ttu-id="e719b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e719b-110">-DefaultProfile</span></span>
<span data-ttu-id="e719b-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e719b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e719b-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e719b-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="e719b-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="e719b-113">-Location</span></span>
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

### <span data-ttu-id="e719b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e719b-114">CommonParameters</span></span>
<span data-ttu-id="e719b-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e719b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e719b-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e719b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e719b-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e719b-117">INPUTS</span></span>

### <span data-ttu-id="e719b-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="e719b-118">None</span></span>

## <span data-ttu-id="e719b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e719b-119">OUTPUTS</span></span>

### <span data-ttu-id="e719b-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e719b-120">System.Boolean</span></span>

## <span data-ttu-id="e719b-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e719b-121">NOTES</span></span>

## <span data-ttu-id="e719b-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e719b-122">RELATED LINKS</span></span>
