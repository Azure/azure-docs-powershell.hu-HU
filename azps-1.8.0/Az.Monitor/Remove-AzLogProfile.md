---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 6b011201dec1c5ef7fd06f503843f7336f5ab220
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670792"
---
# <span data-ttu-id="6867d-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6867d-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="6867d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6867d-102">SYNOPSIS</span></span>
<span data-ttu-id="6867d-103">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6867d-103">Removes a log profile.</span></span>

## <span data-ttu-id="6867d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6867d-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6867d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6867d-105">DESCRIPTION</span></span>
<span data-ttu-id="6867d-106">A **Remove-AzLogProfile** parancsmag eltávolít egy log-profilt.</span><span class="sxs-lookup"><span data-stu-id="6867d-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="6867d-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="6867d-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="6867d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6867d-108">EXAMPLES</span></span>

## <span data-ttu-id="6867d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6867d-109">PARAMETERS</span></span>

### <span data-ttu-id="6867d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6867d-110">-DefaultProfile</span></span>
<span data-ttu-id="6867d-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6867d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6867d-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6867d-112">-Name</span></span>
<span data-ttu-id="6867d-113">Az eltávolítandó naplózási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6867d-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="6867d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6867d-114">-PassThru</span></span>
<span data-ttu-id="6867d-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6867d-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6867d-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6867d-116">-Confirm</span></span>
<span data-ttu-id="6867d-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6867d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6867d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6867d-118">-WhatIf</span></span>
<span data-ttu-id="6867d-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6867d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6867d-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6867d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6867d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6867d-121">CommonParameters</span></span>
<span data-ttu-id="6867d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6867d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6867d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6867d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6867d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6867d-124">INPUTS</span></span>

### <span data-ttu-id="6867d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6867d-125">System.String</span></span>

## <span data-ttu-id="6867d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6867d-126">OUTPUTS</span></span>

### <span data-ttu-id="6867d-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6867d-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="6867d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6867d-128">NOTES</span></span>

## <span data-ttu-id="6867d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6867d-129">RELATED LINKS</span></span>

[<span data-ttu-id="6867d-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6867d-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="6867d-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="6867d-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


