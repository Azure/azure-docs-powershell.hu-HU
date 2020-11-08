---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194319"
---
# <span data-ttu-id="f5056-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f5056-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="f5056-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5056-102">SYNOPSIS</span></span>
<span data-ttu-id="f5056-103">Egy vagy több tevékenység naplója riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="f5056-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="f5056-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5056-104">SYNTAX</span></span>

### <span data-ttu-id="f5056-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5056-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5056-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5056-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5056-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5056-107">DESCRIPTION</span></span>
<span data-ttu-id="f5056-108">A **Get-AzActivityLogAlert** parancsmag egy vagy több tevékenység naplójának riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="f5056-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="f5056-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5056-109">EXAMPLES</span></span>

### <span data-ttu-id="f5056-110">Példa 1: műveletnapló értesítéseinek beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="f5056-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="f5056-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes tevékenység-naplózási értesítést.</span><span class="sxs-lookup"><span data-stu-id="f5056-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="f5056-112">2. példa: tevékenység-naplózási értesítések beszerzése az adott erőforráscsoport számára</span><span class="sxs-lookup"><span data-stu-id="f5056-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="f5056-113">Ez a parancs megjeleníti a műveletnapló riasztásait az adott erőforráscsoport számára.</span><span class="sxs-lookup"><span data-stu-id="f5056-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="f5056-114">3. példa: tevékenység-naplózási riasztás kérése</span><span class="sxs-lookup"><span data-stu-id="f5056-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="f5056-115">Ez a parancs egy (egyetlen elemmel rendelkező) tevékenység-naplózási riasztást sorol fel.</span><span class="sxs-lookup"><span data-stu-id="f5056-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="f5056-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5056-116">PARAMETERS</span></span>

### <span data-ttu-id="f5056-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5056-117">-DefaultProfile</span></span>
<span data-ttu-id="f5056-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f5056-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5056-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5056-119">-Name</span></span>
<span data-ttu-id="f5056-120">A műveletnapló riasztásának neve.</span><span class="sxs-lookup"><span data-stu-id="f5056-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="f5056-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5056-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5056-122">Annak az erőforráscsoportnek a neve, amelyben az értesítési erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="f5056-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="f5056-123">Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="f5056-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="f5056-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5056-124">CommonParameters</span></span>
<span data-ttu-id="f5056-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5056-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5056-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5056-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5056-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5056-127">INPUTS</span></span>

### <span data-ttu-id="f5056-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f5056-128">System.String</span></span>

## <span data-ttu-id="f5056-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5056-129">OUTPUTS</span></span>

### <span data-ttu-id="f5056-130">Microsoft. Azure. commands. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f5056-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f5056-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5056-131">NOTES</span></span>

## <span data-ttu-id="f5056-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5056-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5056-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f5056-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f5056-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f5056-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="f5056-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f5056-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="f5056-136">Új – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f5056-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="f5056-137">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f5056-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)