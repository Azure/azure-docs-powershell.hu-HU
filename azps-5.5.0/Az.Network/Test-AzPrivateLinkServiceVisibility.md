---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158771"
---
# <span data-ttu-id="929b9-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="929b9-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="929b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="929b9-102">SYNOPSIS</span></span>
<span data-ttu-id="929b9-103">A **Test-AzPrivateLinkServiceVisibility** ellenőrzi, hogy látható-e egy privát hivatkozásszolgáltatás az aktuális használatra.</span><span class="sxs-lookup"><span data-stu-id="929b9-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="929b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="929b9-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="929b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="929b9-105">DESCRIPTION</span></span>
<span data-ttu-id="929b9-106">Ellenőrizze, hogy látható-e egy privát hivatkozásszolgáltatás az aktuális használatra.</span><span class="sxs-lookup"><span data-stu-id="929b9-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="929b9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="929b9-107">EXAMPLES</span></span>

### <span data-ttu-id="929b9-108">1. példa: Ellenőrizze, contoso.cloudapp.azure.com elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="929b9-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="929b9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="929b9-109">PARAMETERS</span></span>

### <span data-ttu-id="929b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929b9-110">-DefaultProfile</span></span>
<span data-ttu-id="929b9-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="929b9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="929b9-112">-Location</span><span class="sxs-lookup"><span data-stu-id="929b9-112">-Location</span></span>
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

### <span data-ttu-id="929b9-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="929b9-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="929b9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="929b9-114">-ResourceGroupName</span></span>
<span data-ttu-id="929b9-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="929b9-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="929b9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929b9-116">CommonParameters</span></span>
<span data-ttu-id="929b9-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="929b9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929b9-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="929b9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929b9-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="929b9-119">INPUTS</span></span>

### <span data-ttu-id="929b9-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="929b9-120">None</span></span>

## <span data-ttu-id="929b9-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="929b9-121">OUTPUTS</span></span>

### <span data-ttu-id="929b9-122">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="929b9-122">System.Boolean</span></span>

## <span data-ttu-id="929b9-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="929b9-123">NOTES</span></span>

## <span data-ttu-id="929b9-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="929b9-124">RELATED LINKS</span></span>
