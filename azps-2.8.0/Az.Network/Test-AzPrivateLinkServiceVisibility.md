---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-azprivatelinkservicevisibility
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzPrivateLinkServiceVisibility.md
ms.openlocfilehash: e05ea63bddc8dc61332a31e4fa44aa1b7428055a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838266"
---
# <span data-ttu-id="aa61f-101">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="aa61f-101">Test-AzPrivateLinkServiceVisibility</span></span>

## <span data-ttu-id="aa61f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa61f-102">SYNOPSIS</span></span>
<span data-ttu-id="aa61f-103">A **AzPrivateLinkServiceVisibility** ellenőrzi, hogy a privát hivatkozás szolgáltatás látható-e a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="aa61f-103">The **Test-AzPrivateLinkServiceVisibility** checks whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="aa61f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa61f-104">SYNTAX</span></span>

```
Test-AzPrivateLinkServiceVisibility -Location <String> [-ResourceGroupName <String>]
 -PrivateLinkServiceAlias <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa61f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa61f-105">DESCRIPTION</span></span>
<span data-ttu-id="aa61f-106">Ellenőrizze, hogy látható-e egy privát hivatkozás szolgáltatás a jelenlegi használathoz.</span><span class="sxs-lookup"><span data-stu-id="aa61f-106">Check whether a private link service is visible for current use.</span></span>

## <span data-ttu-id="aa61f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa61f-107">EXAMPLES</span></span>

### <span data-ttu-id="aa61f-108">Példa 1: annak ellenőrzése, hogy elérhető-e a contoso.cloudapp.azure.com.</span><span class="sxs-lookup"><span data-stu-id="aa61f-108">Example 1: Check if contoso.cloudapp.azure.com is available for use.</span></span>
```
Test-AzPrivateLinkServiceVisibility -Location westus -PrivateLinkServiceAlias "TestPLS.00000000-0000-0000-0000-000000000000.azure.privatelinkservice"
```

## <span data-ttu-id="aa61f-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa61f-109">PARAMETERS</span></span>

### <span data-ttu-id="aa61f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa61f-110">-DefaultProfile</span></span>
<span data-ttu-id="aa61f-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa61f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa61f-112">-Hely</span><span class="sxs-lookup"><span data-stu-id="aa61f-112">-Location</span></span>
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

### <span data-ttu-id="aa61f-113">-PrivateLinkServiceAlias</span><span class="sxs-lookup"><span data-stu-id="aa61f-113">-PrivateLinkServiceAlias</span></span>
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

### <span data-ttu-id="aa61f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa61f-114">-ResourceGroupName</span></span>
<span data-ttu-id="aa61f-115">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa61f-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aa61f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa61f-116">CommonParameters</span></span>
<span data-ttu-id="aa61f-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa61f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa61f-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa61f-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa61f-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa61f-119">INPUTS</span></span>

### <span data-ttu-id="aa61f-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="aa61f-120">None</span></span>

## <span data-ttu-id="aa61f-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa61f-121">OUTPUTS</span></span>

### <span data-ttu-id="aa61f-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa61f-122">System.Boolean</span></span>

## <span data-ttu-id="aa61f-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa61f-123">NOTES</span></span>

## <span data-ttu-id="aa61f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa61f-124">RELATED LINKS</span></span>
