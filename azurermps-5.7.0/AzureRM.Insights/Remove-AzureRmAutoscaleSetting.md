---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494500"
---
# <span data-ttu-id="88413-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="88413-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="88413-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88413-102">SYNOPSIS</span></span>
<span data-ttu-id="88413-103">Az automéretarány beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="88413-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88413-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88413-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88413-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88413-105">DESCRIPTION</span></span>
<span data-ttu-id="88413-106">A **Remove-AzureRmAutoscaleSetting** parancsmag automatikusan eltávolítja az automéretarány beállítást.</span><span class="sxs-lookup"><span data-stu-id="88413-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="88413-107">Meg kell adnia a beállítás nevét, valamint annak az erőforrás-csoportnak a nevét, amelyhez hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="88413-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="88413-108">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="88413-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="88413-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88413-109">EXAMPLES</span></span>

## <span data-ttu-id="88413-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88413-110">PARAMETERS</span></span>

### <span data-ttu-id="88413-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88413-111">-DefaultProfile</span></span>
<span data-ttu-id="88413-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="88413-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88413-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88413-113">-Name</span></span>
<span data-ttu-id="88413-114">Az eltávolítandó méretezési beállítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88413-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="88413-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88413-115">-ResourceGroupName</span></span>
<span data-ttu-id="88413-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88413-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88413-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88413-117">CommonParameters</span></span>
<span data-ttu-id="88413-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88413-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88413-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88413-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88413-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88413-120">INPUTS</span></span>

### <span data-ttu-id="88413-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="88413-121">None</span></span>
<span data-ttu-id="88413-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="88413-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88413-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88413-123">OUTPUTS</span></span>

### <span data-ttu-id="88413-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="88413-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="88413-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88413-125">NOTES</span></span>

## <span data-ttu-id="88413-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88413-126">RELATED LINKS</span></span>

[<span data-ttu-id="88413-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="88413-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="88413-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="88413-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


