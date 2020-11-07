---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679705"
---
# <span data-ttu-id="c157a-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="c157a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c157a-102">SYNOPSIS</span></span>
<span data-ttu-id="c157a-103">Begyűjtheti a beosztásokat.</span><span class="sxs-lookup"><span data-stu-id="c157a-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c157a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c157a-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c157a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c157a-105">DESCRIPTION</span></span>
<span data-ttu-id="c157a-106">A **Get-AzureRmSchedulerJobCollection** parancsmag az Azure Scheduler webhelyének munkagyűjteményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="c157a-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="c157a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c157a-107">EXAMPLES</span></span>

## <span data-ttu-id="c157a-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c157a-108">PARAMETERS</span></span>

### <span data-ttu-id="c157a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c157a-109">-DefaultProfile</span></span>
<span data-ttu-id="c157a-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c157a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c157a-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="c157a-111">-JobCollectionName</span></span>
<span data-ttu-id="c157a-112">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c157a-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c157a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c157a-113">-ResourceGroupName</span></span>
<span data-ttu-id="c157a-114">Azt az erőforráscsoport-csoportot adja meg, amelyből a parancsmag begyűjti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="c157a-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c157a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c157a-115">CommonParameters</span></span>
<span data-ttu-id="c157a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c157a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c157a-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c157a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c157a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c157a-118">INPUTS</span></span>

### <span data-ttu-id="c157a-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="c157a-119">None</span></span>
<span data-ttu-id="c157a-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="c157a-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c157a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c157a-121">OUTPUTS</span></span>

### <span data-ttu-id="c157a-122">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c157a-122">System.Object</span></span>

## <span data-ttu-id="c157a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c157a-123">NOTES</span></span>

## <span data-ttu-id="c157a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c157a-124">RELATED LINKS</span></span>

[<span data-ttu-id="c157a-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c157a-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c157a-127">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c157a-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="c157a-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="c157a-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


