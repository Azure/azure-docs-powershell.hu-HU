---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494492"
---
# <span data-ttu-id="312d2-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="312d2-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="312d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="312d2-102">SYNOPSIS</span></span>
<span data-ttu-id="312d2-103">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="312d2-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="312d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="312d2-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="312d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="312d2-105">DESCRIPTION</span></span>
<span data-ttu-id="312d2-106">A **Remove-AzureRmLogProfile** parancsmag eltávolít egy log-profilt.</span><span class="sxs-lookup"><span data-stu-id="312d2-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="312d2-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="312d2-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="312d2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="312d2-108">EXAMPLES</span></span>

## <span data-ttu-id="312d2-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="312d2-109">PARAMETERS</span></span>

### <span data-ttu-id="312d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="312d2-110">-DefaultProfile</span></span>
<span data-ttu-id="312d2-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="312d2-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312d2-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="312d2-112">-Name</span></span>
<span data-ttu-id="312d2-113">Az eltávolítandó naplózási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="312d2-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312d2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="312d2-114">-PassThru</span></span>
<span data-ttu-id="312d2-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="312d2-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="312d2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="312d2-116">CommonParameters</span></span>
<span data-ttu-id="312d2-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="312d2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="312d2-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="312d2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="312d2-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="312d2-119">INPUTS</span></span>

### <span data-ttu-id="312d2-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="312d2-120">None</span></span>
<span data-ttu-id="312d2-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="312d2-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="312d2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="312d2-122">OUTPUTS</span></span>

### <span data-ttu-id="312d2-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="312d2-123">AzureOperationResponse</span></span>

## <span data-ttu-id="312d2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="312d2-124">NOTES</span></span>

## <span data-ttu-id="312d2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="312d2-125">RELATED LINKS</span></span>

[<span data-ttu-id="312d2-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="312d2-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="312d2-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="312d2-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


