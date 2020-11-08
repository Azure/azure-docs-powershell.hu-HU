---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181501"
---
# <span data-ttu-id="5028e-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="5028e-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="5028e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5028e-102">SYNOPSIS</span></span>
<span data-ttu-id="5028e-103">A **AzPrivateLinkServiceVisibility** ellenőrzi, hogy a privát hivatkozás szolgáltatás látható-e a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="5028e-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="5028e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5028e-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5028e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5028e-105">DESCRIPTION</span></span>
<span data-ttu-id="5028e-106">Ellenőrizze, hogy látható-e egy privát hivatkozás szolgáltatás a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="5028e-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="5028e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5028e-107">EXAMPLES</span></span>

### <span data-ttu-id="5028e-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="5028e-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="5028e-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5028e-109">PARAMETERS</span></span>

### <span data-ttu-id="5028e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5028e-110">-DefaultProfile</span></span>
<span data-ttu-id="5028e-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5028e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5028e-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="5028e-112">-Location</span></span>
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

### <span data-ttu-id="5028e-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="5028e-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="5028e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5028e-114">-ResourceGroupName</span></span>
<span data-ttu-id="5028e-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5028e-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5028e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5028e-116">CommonParameters</span></span>
<span data-ttu-id="5028e-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5028e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5028e-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5028e-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5028e-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5028e-119">INPUTS</span></span>

### <span data-ttu-id="5028e-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="5028e-120">None</span></span>

## <span data-ttu-id="5028e-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5028e-121">OUTPUTS</span></span>

### <span data-ttu-id="5028e-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5028e-122">System.Boolean</span></span>

## <span data-ttu-id="5028e-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5028e-123">NOTES</span></span>

## <span data-ttu-id="5028e-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5028e-124">RELATED LINKS</span></span>
