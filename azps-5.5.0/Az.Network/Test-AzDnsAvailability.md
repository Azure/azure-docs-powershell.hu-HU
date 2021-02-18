---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 556A9F12-DF72-468F-9C3F-A747CC70BD2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azdnsavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzDnsAvailability.md
ms.openlocfilehash: 2ee468c47f22e90ce47b003dcae1becfb905134e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202383"
---
# <span data-ttu-id="0210b-101">Test-AzDnsAvailability</span><span class="sxs-lookup"><span data-stu-id="0210b-101">Test-AzDnsAvailability</span></span>

## <span data-ttu-id="0210b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0210b-102">SYNOPSIS</span></span>
<span data-ttu-id="0210b-103">Annak ellenőrzése, hogy használható-e tartománynév a cloudapp.azure.com zónában.</span><span class="sxs-lookup"><span data-stu-id="0210b-103">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="0210b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0210b-104">SYNTAX</span></span>

```
Test-AzDnsAvailability -DomainNameLabel <String> -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0210b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0210b-105">DESCRIPTION</span></span>
<span data-ttu-id="0210b-106">Annak ellenőrzése, hogy használható-e tartománynév a cloudapp.azure.com zónában.</span><span class="sxs-lookup"><span data-stu-id="0210b-106">Checks whether a domain name in the cloudapp.azure.com zone is available for use.</span></span>

## <span data-ttu-id="0210b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0210b-107">EXAMPLES</span></span>

### <span data-ttu-id="0210b-108">1. példa: Ellenőrizze, contoso.westus.cloudapp.azure.com a contoso.westus.cloudapp.azure.com használható-e.</span><span class="sxs-lookup"><span data-stu-id="0210b-108">Example 1: Check if contoso.westus.cloudapp.azure.com is available for use.</span></span>
```
Test-AzDnsAvailability -DomainNameLabel contoso -Location westus
```

## <span data-ttu-id="0210b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0210b-109">PARAMETERS</span></span>

### <span data-ttu-id="0210b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0210b-110">-DefaultProfile</span></span>
<span data-ttu-id="0210b-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0210b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0210b-112">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="0210b-112">-DomainNameLabel</span></span>
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

### <span data-ttu-id="0210b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0210b-113">-Location</span></span>
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

### <span data-ttu-id="0210b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0210b-114">CommonParameters</span></span>
<span data-ttu-id="0210b-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0210b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0210b-116">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0210b-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0210b-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0210b-117">INPUTS</span></span>

### <span data-ttu-id="0210b-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="0210b-118">None</span></span>

## <span data-ttu-id="0210b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0210b-119">OUTPUTS</span></span>

### <span data-ttu-id="0210b-120">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0210b-120">System.Boolean</span></span>

## <span data-ttu-id="0210b-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0210b-121">NOTES</span></span>

## <span data-ttu-id="0210b-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0210b-122">RELATED LINKS</span></span>
