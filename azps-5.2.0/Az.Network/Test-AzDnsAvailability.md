---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363382"
---
# <span data-ttu-id="791d3-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="791d3-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="791d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="791d3-102">SYNOPSIS</span></span>
<span data-ttu-id="791d3-103">Annak ellenőrzése, hogy használható-e tartománynév a cloudapp.azure.com zónában.</span><span class="sxs-lookup"><span data-stu-id="791d3-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="791d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="791d3-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="791d3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="791d3-105">DESCRIPTION</span></span>
<span data-ttu-id="791d3-106">Annak ellenőrzése, hogy használható-e tartománynév a cloudapp.azure.com zónában.</span><span class="sxs-lookup"><span data-stu-id="791d3-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="791d3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="791d3-107">EXAMPLES</span></span>

### <span data-ttu-id="791d3-108">1. példa: Ellenőrizze, contoso.westus.cloudapp.azure.com elérhető-e az alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="791d3-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="791d3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="791d3-109">PARAMETERS</span></span>

### <span data-ttu-id="791d3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791d3-110">-DefaultProfile</span></span>
<span data-ttu-id="791d3-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="791d3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="791d3-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="791d3-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="791d3-113">-Location</span><span class="sxs-lookup"><span data-stu-id="791d3-113">-Location</span></span>
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

### <span data-ttu-id="791d3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791d3-114">CommonParameters</span></span>
<span data-ttu-id="791d3-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="791d3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791d3-116">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791d3-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791d3-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="791d3-117">INPUTS</span></span>

### <span data-ttu-id="791d3-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="791d3-118">None</span></span>

## <span data-ttu-id="791d3-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="791d3-119">OUTPUTS</span></span>

### <span data-ttu-id="791d3-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="791d3-120">System.Boolean</span></span>

## <span data-ttu-id="791d3-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="791d3-121">NOTES</span></span>

## <span data-ttu-id="791d3-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="791d3-122">RELATED LINKS</span></span>
