---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92550ee9f5eed7cf31624748140a0355ac6849ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680112"
---
# <span data-ttu-id="67ea8-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="67ea8-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="67ea8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="67ea8-103">Egy vagy több tevékenység naplója riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="67ea8-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67ea8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67ea8-104">SYNTAX</span></span>

### <span data-ttu-id="67ea8-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67ea8-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ea8-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="67ea8-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67ea8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="67ea8-107">DESCRIPTION</span></span>
<span data-ttu-id="67ea8-108">A **Get-AzureRmActivityLogAlert** parancsmag egy vagy több tevékenység naplójának riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="67ea8-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="67ea8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="67ea8-109">EXAMPLES</span></span>

### <span data-ttu-id="67ea8-110">Példa 1: műveletnapló értesítéseinek beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="67ea8-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="67ea8-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes tevékenység-naplózási értesítést.</span><span class="sxs-lookup"><span data-stu-id="67ea8-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="67ea8-112">2. példa: tevékenység-naplózási értesítések beszerzése az adott erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="67ea8-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="67ea8-113">Ez a parancs megjeleníti a műveletnapló riasztásait az adott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="67ea8-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="67ea8-114">3. példa: tevékenység-naplózási riasztás kérése</span><span class="sxs-lookup"><span data-stu-id="67ea8-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="67ea8-115">Ez a parancs egy (egyetlen elemmel rendelkező) tevékenység-naplózási riasztást sorol fel.</span><span class="sxs-lookup"><span data-stu-id="67ea8-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="67ea8-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67ea8-116">PARAMETERS</span></span>

### <span data-ttu-id="67ea8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ea8-117">-DefaultProfile</span></span>
<span data-ttu-id="67ea8-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="67ea8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67ea8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="67ea8-119">-Name</span></span>
<span data-ttu-id="67ea8-120">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="67ea8-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ea8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ea8-121">-ResourceGroupName</span></span>
<span data-ttu-id="67ea8-122">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="67ea8-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="67ea8-123">Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="67ea8-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67ea8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ea8-124">CommonParameters</span></span>
<span data-ttu-id="67ea8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67ea8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ea8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ea8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ea8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67ea8-127">INPUTS</span></span>

### <span data-ttu-id="67ea8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="67ea8-128">System.String</span></span>

## <span data-ttu-id="67ea8-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67ea8-129">OUTPUTS</span></span>

### <span data-ttu-id="67ea8-130">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="67ea8-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="67ea8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67ea8-131">NOTES</span></span>

## <span data-ttu-id="67ea8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67ea8-132">RELATED LINKS</span></span>

[<span data-ttu-id="67ea8-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="67ea8-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="67ea8-134">Update-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="67ea8-134">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="67ea8-135">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="67ea8-135">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="67ea8-136">Új – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="67ea8-136">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="67ea8-137">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="67ea8-137">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
