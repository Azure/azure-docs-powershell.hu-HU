---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: 3fe05034734a4cfb0d511921372e41b00d7b457c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918473"
---
# <span data-ttu-id="fb0d1-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="fb0d1-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="fb0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb0d1-103">A **Test-AzPrivateLinkServiceVisibility** ellenőrzi, hogy látható-e egy privát hivatkozásszolgáltatás az aktuális használatra.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="fb0d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb0d1-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb0d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb0d1-105">DESCRIPTION</span></span>
<span data-ttu-id="fb0d1-106">Ellenőrizze, hogy látható-e egy privát hivatkozásszolgáltatás az aktuális használatra.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="fb0d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb0d1-107">EXAMPLES</span></span>

### <span data-ttu-id="fb0d1-108">1. példa: Ellenőrizze, contoso.cloudapp.azure.com elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="fb0d1-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb0d1-109">PARAMETERS</span></span>

### <span data-ttu-id="fb0d1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb0d1-110">-DefaultProfile</span></span>
<span data-ttu-id="fb0d1-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb0d1-112">-Location</span><span class="sxs-lookup"><span data-stu-id="fb0d1-112">-Location</span></span>
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

### <span data-ttu-id="fb0d1-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="fb0d1-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="fb0d1-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb0d1-114">-ResourceGroupName</span></span>
<span data-ttu-id="fb0d1-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fb0d1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb0d1-116">CommonParameters</span></span>
<span data-ttu-id="fb0d1-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb0d1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb0d1-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb0d1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb0d1-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb0d1-119">INPUTS</span></span>

### <span data-ttu-id="fb0d1-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb0d1-120">None</span></span>

## <span data-ttu-id="fb0d1-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb0d1-121">OUTPUTS</span></span>

### <span data-ttu-id="fb0d1-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb0d1-122">System.Boolean</span></span>

## <span data-ttu-id="fb0d1-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb0d1-123">NOTES</span></span>

## <span data-ttu-id="fb0d1-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb0d1-124">RELATED LINKS</span></span>
