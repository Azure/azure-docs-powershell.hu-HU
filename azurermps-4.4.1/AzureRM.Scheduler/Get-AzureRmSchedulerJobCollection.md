---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504736"
---
# <span data-ttu-id="b3706-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="b3706-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3706-102">SYNOPSIS</span></span>
<span data-ttu-id="b3706-103">Begyűjtheti a beosztásokat.</span><span class="sxs-lookup"><span data-stu-id="b3706-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3706-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3706-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3706-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3706-105">DESCRIPTION</span></span>
<span data-ttu-id="b3706-106">A **Get-AzureRmSchedulerJobCollection** parancsmag az Azure Scheduler webhelyének munkagyűjteményeit kapja.</span><span class="sxs-lookup"><span data-stu-id="b3706-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="b3706-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3706-107">EXAMPLES</span></span>

## <span data-ttu-id="b3706-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3706-108">PARAMETERS</span></span>

### <span data-ttu-id="b3706-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="b3706-109">-JobCollectionName</span></span>
<span data-ttu-id="b3706-110">A begyűjtő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3706-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3706-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3706-111">-ResourceGroupName</span></span>
<span data-ttu-id="b3706-112">Azt az erőforráscsoport-csoportot adja meg, amelyből a parancsmag begyűjti a feladatot.</span><span class="sxs-lookup"><span data-stu-id="b3706-112">Specifies resource group from which this cmdlet gets job collections.</span></span>

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

### <span data-ttu-id="b3706-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3706-113">-DefaultProfile</span></span>
<span data-ttu-id="b3706-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3706-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3706-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3706-115">CommonParameters</span></span>
<span data-ttu-id="b3706-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3706-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3706-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3706-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3706-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3706-118">INPUTS</span></span>

## <span data-ttu-id="b3706-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3706-119">OUTPUTS</span></span>

### <span data-ttu-id="b3706-120">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="b3706-120">System.Object</span></span>

## <span data-ttu-id="b3706-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3706-121">NOTES</span></span>

## <span data-ttu-id="b3706-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3706-122">RELATED LINKS</span></span>

[<span data-ttu-id="b3706-123">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-123">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b3706-124">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-124">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b3706-125">Új – AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-125">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b3706-126">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-126">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="b3706-127">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="b3706-127">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


