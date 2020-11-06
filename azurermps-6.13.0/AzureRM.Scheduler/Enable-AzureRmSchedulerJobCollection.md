---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: BA79EDC8-BE89-4836-92EF-748D6F518886
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/enable-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Enable-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: db2229ed6a0bc5f83dc3d0e856a22b846309ee42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505272"
---
# <span data-ttu-id="c8418-101">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-101">Enable-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="c8418-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c8418-102">SYNOPSIS</span></span>
<span data-ttu-id="c8418-103">Begyűjtheti a beosztást.</span><span class="sxs-lookup"><span data-stu-id="c8418-103">Enables a job collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8418-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c8418-104">SYNTAX</span></span>

```
Enable-AzureRmSchedulerJobCollection -ResourceGroupName <String> -JobCollectionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8418-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c8418-105">DESCRIPTION</span></span>
<span data-ttu-id="c8418-106">Az **enable-AzureRmSchedulerJobCollection** parancsmag lehetővé teszi a begyűjtést az Azure schedulerben.</span><span class="sxs-lookup"><span data-stu-id="c8418-106">The **Enable-AzureRmSchedulerJobCollection** cmdlet enables a job collection in Azure Scheduler.</span></span>

## <span data-ttu-id="c8418-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c8418-107">EXAMPLES</span></span>

## <span data-ttu-id="c8418-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c8418-108">PARAMETERS</span></span>

### <span data-ttu-id="c8418-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8418-109">-DefaultProfile</span></span>
<span data-ttu-id="c8418-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8418-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8418-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c8418-111">-JobCollectionName</span></span>
<span data-ttu-id="c8418-112">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8418-112">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8418-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8418-113">-PassThru</span></span>
<span data-ttu-id="c8418-114">Jelzi, hogy ez a parancsmag a siker sikerének értékét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c8418-114">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="c8418-115">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c8418-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c8418-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8418-116">-ResourceGroupName</span></span>
<span data-ttu-id="c8418-117">A begyűjtő erőforrás csoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8418-117">Specifies the resource group of the job collection.</span></span>

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

### <span data-ttu-id="c8418-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c8418-118">-Confirm</span></span>
<span data-ttu-id="c8418-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c8418-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8418-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8418-120">-WhatIf</span></span>
<span data-ttu-id="c8418-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c8418-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8418-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c8418-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8418-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8418-123">CommonParameters</span></span>
<span data-ttu-id="c8418-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c8418-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8418-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8418-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8418-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8418-126">INPUTS</span></span>

### <span data-ttu-id="c8418-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c8418-127">System.String</span></span>

## <span data-ttu-id="c8418-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8418-128">OUTPUTS</span></span>

### <span data-ttu-id="c8418-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c8418-129">System.String</span></span>

## <span data-ttu-id="c8418-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c8418-130">NOTES</span></span>

## <span data-ttu-id="c8418-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8418-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8418-132">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-132">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8418-133">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-133">Get-AzureRmSchedulerJobCollection</span></span>](./Get-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8418-134">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-134">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8418-135">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-135">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c8418-136">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c8418-136">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


