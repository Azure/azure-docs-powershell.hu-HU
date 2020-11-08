---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94172838"
---
# <span data-ttu-id="25fc6-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="25fc6-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="25fc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="25fc6-103">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="25fc6-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="25fc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25fc6-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25fc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="25fc6-106">Ellenőrzi, hogy elérhető-e egy tartománynév a cloudapp.azure.com-zónában.</span><span class="sxs-lookup"><span data-stu-id="25fc6-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="25fc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="25fc6-107">EXAMPLES</span></span>

### <span data-ttu-id="25fc6-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.westus.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="25fc6-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="25fc6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25fc6-109">PARAMETERS</span></span>

### <span data-ttu-id="25fc6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25fc6-110">-DefaultProfile</span></span>
<span data-ttu-id="25fc6-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25fc6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25fc6-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="25fc6-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="25fc6-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="25fc6-113">-Location</span></span>
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

### <span data-ttu-id="25fc6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25fc6-114">CommonParameters</span></span>
<span data-ttu-id="25fc6-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25fc6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25fc6-116">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25fc6-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25fc6-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25fc6-117">INPUTS</span></span>

### <span data-ttu-id="25fc6-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="25fc6-118">None</span></span>

## <span data-ttu-id="25fc6-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25fc6-119">OUTPUTS</span></span>

### <span data-ttu-id="25fc6-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25fc6-120">System.Boolean</span></span>

## <span data-ttu-id="25fc6-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25fc6-121">NOTES</span></span>

## <span data-ttu-id="25fc6-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25fc6-122">RELATED LINKS</span></span>
