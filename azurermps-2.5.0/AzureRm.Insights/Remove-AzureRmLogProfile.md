---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848278"
---
# <span data-ttu-id="47dee-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="47dee-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="47dee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47dee-102">SYNOPSIS</span></span>
<span data-ttu-id="47dee-103">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="47dee-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47dee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47dee-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47dee-105">DESCRIPTION</span></span>
<span data-ttu-id="47dee-106">A **Remove-AzureRmLogProfile** parancsmag eltávolít egy log-profilt.</span><span class="sxs-lookup"><span data-stu-id="47dee-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="47dee-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="47dee-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="47dee-108">Példák</span><span class="sxs-lookup"><span data-stu-id="47dee-108">EXAMPLES</span></span>

## <span data-ttu-id="47dee-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47dee-109">PARAMETERS</span></span>

### <span data-ttu-id="47dee-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dee-110">-DefaultProfile</span></span>
<span data-ttu-id="47dee-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="47dee-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dee-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47dee-112">-Name</span></span>
<span data-ttu-id="47dee-113">Az eltávolítandó naplózási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47dee-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="47dee-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47dee-114">-PassThru</span></span>
<span data-ttu-id="47dee-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="47dee-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dee-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="47dee-116">-Confirm</span></span>
<span data-ttu-id="47dee-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="47dee-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dee-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dee-118">-WhatIf</span></span>
<span data-ttu-id="47dee-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="47dee-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47dee-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="47dee-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dee-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dee-121">CommonParameters</span></span>
<span data-ttu-id="47dee-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47dee-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dee-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47dee-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dee-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47dee-124">INPUTS</span></span>

### <span data-ttu-id="47dee-125">System. String</span><span class="sxs-lookup"><span data-stu-id="47dee-125">System.String</span></span>

## <span data-ttu-id="47dee-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47dee-126">OUTPUTS</span></span>

### <span data-ttu-id="47dee-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47dee-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="47dee-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47dee-128">NOTES</span></span>

## <span data-ttu-id="47dee-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47dee-129">RELATED LINKS</span></span>

[<span data-ttu-id="47dee-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="47dee-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="47dee-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="47dee-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


