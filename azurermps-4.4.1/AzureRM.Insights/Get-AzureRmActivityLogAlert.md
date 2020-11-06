---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504943"
---
# <span data-ttu-id="aaa82-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aaa82-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="aaa82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aaa82-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa82-103">Egy vagy több tevékenység naplója riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="aaa82-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaa82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aaa82-104">SYNTAX</span></span>

### <span data-ttu-id="aaa82-105">Az alapértelmezett paraméterek a tevékenység-naplózási riasztás beszerzéséhez</span><span class="sxs-lookup"><span data-stu-id="aaa82-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aaa82-106">Paraméterek, amelyekkel meggyőződhet arról, hogy a név megadásakor az erőforráscsoport meg van adva</span><span class="sxs-lookup"><span data-stu-id="aaa82-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaa82-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aaa82-107">DESCRIPTION</span></span>
<span data-ttu-id="aaa82-108">A **Get-AzureRmActivityLogAlert** parancsmag egy vagy több tevékenység naplójának riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="aaa82-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="aaa82-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aaa82-109">EXAMPLES</span></span>

### <span data-ttu-id="aaa82-110">Példa 1: műveletnapló értesítéseinek beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="aaa82-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="aaa82-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes tevékenység-naplózási értesítést.</span><span class="sxs-lookup"><span data-stu-id="aaa82-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="aaa82-112">2. példa: tevékenység-naplózási értesítések beszerzése az adott erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="aaa82-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="aaa82-113">Ez a parancs megjeleníti a műveletnapló riasztásait az adott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="aaa82-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="aaa82-114">3. példa: tevékenység-naplózási riasztás kérése</span><span class="sxs-lookup"><span data-stu-id="aaa82-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="aaa82-115">Ez a parancs egy (egyetlen elemmel rendelkező) tevékenység-naplózási riasztást sorol fel.</span><span class="sxs-lookup"><span data-stu-id="aaa82-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="aaa82-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aaa82-116">PARAMETERS</span></span>

### <span data-ttu-id="aaa82-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aaa82-117">-Name</span></span>
<span data-ttu-id="aaa82-118">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="aaa82-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa82-119">-ResourceGroupName</span></span>
<span data-ttu-id="aaa82-120">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="aaa82-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="aaa82-121">Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="aaa82-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaa82-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa82-122">-DefaultProfile</span></span>
<span data-ttu-id="aaa82-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaa82-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaa82-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa82-124">CommonParameters</span></span>
<span data-ttu-id="aaa82-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aaa82-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa82-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa82-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa82-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaa82-127">INPUTS</span></span>

### <span data-ttu-id="aaa82-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="aaa82-128">None</span></span>

## <span data-ttu-id="aaa82-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaa82-129">OUTPUTS</span></span>

### <span data-ttu-id="aaa82-130"><System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintést. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="aaa82-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="aaa82-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="aaa82-131">None</span></span>

## <span data-ttu-id="aaa82-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aaa82-132">NOTES</span></span>

## <span data-ttu-id="aaa82-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaa82-133">RELATED LINKS</span></span>

[<span data-ttu-id="aaa82-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aaa82-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="aaa82-135">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aaa82-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="aaa82-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="aaa82-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="aaa82-137">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="aaa82-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="aaa82-138">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="aaa82-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
