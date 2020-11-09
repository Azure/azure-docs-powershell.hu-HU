---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: f443928a8a616e8b8c6c13e5ae941aff607638ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303080"
---
# <span data-ttu-id="94fb7-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="94fb7-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="94fb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="94fb7-103">A **AzPrivateLinkServiceVisibility** ellenőrzi, hogy a privát hivatkozás szolgáltatás látható-e a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="94fb7-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="94fb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94fb7-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94fb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="94fb7-106">Ellenőrizze, hogy látható-e egy privát hivatkozás szolgáltatás a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="94fb7-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="94fb7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="94fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="94fb7-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="94fb7-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="94fb7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94fb7-109">PARAMETERS</span></span>

### <span data-ttu-id="94fb7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94fb7-110">-DefaultProfile</span></span>
<span data-ttu-id="94fb7-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94fb7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94fb7-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="94fb7-112">-Location</span></span>
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

### <span data-ttu-id="94fb7-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="94fb7-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="94fb7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94fb7-114">-ResourceGroupName</span></span>
<span data-ttu-id="94fb7-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94fb7-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="94fb7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94fb7-116">CommonParameters</span></span>
<span data-ttu-id="94fb7-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94fb7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94fb7-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94fb7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94fb7-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fb7-119">INPUTS</span></span>

### <span data-ttu-id="94fb7-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="94fb7-120">None</span></span>

## <span data-ttu-id="94fb7-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94fb7-121">OUTPUTS</span></span>

### <span data-ttu-id="94fb7-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94fb7-122">System.Boolean</span></span>

## <span data-ttu-id="94fb7-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94fb7-123">NOTES</span></span>

## <span data-ttu-id="94fb7-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94fb7-124">RELATED LINKS</span></span>
