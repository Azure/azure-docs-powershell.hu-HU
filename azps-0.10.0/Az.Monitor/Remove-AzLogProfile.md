---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: c598b81990bd24d5808c48aa9511ada2dee2852e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841926"
---
# <span data-ttu-id="eb6dc-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb6dc-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="eb6dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6dc-103">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-103">Removes a log profile.</span></span>

## <span data-ttu-id="eb6dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb6dc-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb6dc-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6dc-106">A **Remove-AzLogProfile** parancsmag eltávolít egy log-profilt.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="eb6dc-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="eb6dc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="eb6dc-108">EXAMPLES</span></span>

## <span data-ttu-id="eb6dc-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb6dc-109">PARAMETERS</span></span>

### <span data-ttu-id="eb6dc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6dc-110">-DefaultProfile</span></span>
<span data-ttu-id="eb6dc-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="eb6dc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb6dc-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eb6dc-112">-Name</span></span>
<span data-ttu-id="eb6dc-113">Az eltávolítandó naplózási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="eb6dc-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb6dc-114">-PassThru</span></span>
<span data-ttu-id="eb6dc-115">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eb6dc-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eb6dc-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eb6dc-116">-Confirm</span></span>
<span data-ttu-id="eb6dc-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb6dc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb6dc-118">-WhatIf</span></span>
<span data-ttu-id="eb6dc-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb6dc-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb6dc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6dc-121">CommonParameters</span></span>
<span data-ttu-id="eb6dc-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb6dc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6dc-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eb6dc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6dc-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb6dc-124">INPUTS</span></span>

### <span data-ttu-id="eb6dc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eb6dc-125">System.String</span></span>

## <span data-ttu-id="eb6dc-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb6dc-126">OUTPUTS</span></span>

### <span data-ttu-id="eb6dc-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb6dc-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="eb6dc-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb6dc-128">NOTES</span></span>

## <span data-ttu-id="eb6dc-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb6dc-129">RELATED LINKS</span></span>

[<span data-ttu-id="eb6dc-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb6dc-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="eb6dc-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="eb6dc-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


