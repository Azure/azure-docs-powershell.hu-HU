---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 526b03fb1d73ab88b43929df143e9825f42c7fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932721"
---
# <span data-ttu-id="bd734-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bd734-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="bd734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd734-102">SYNOPSIS</span></span>
<span data-ttu-id="bd734-103">Egy vagy több tevékenységnapló-riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="bd734-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="bd734-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd734-104">SYNTAX</span></span>

### <span data-ttu-id="bd734-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd734-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd734-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd734-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd734-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd734-107">DESCRIPTION</span></span>
<span data-ttu-id="bd734-108">A **Get-AzActivityLogAlert** parancsmag egy vagy több tevékenységnapló-riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="bd734-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="bd734-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd734-109">EXAMPLES</span></span>

### <span data-ttu-id="bd734-110">1. példa: Tevékenységnapló-riasztások lekértése előfizetésazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="bd734-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="bd734-111">Ez a parancs felsorolja az aktuális előfizetés összes tevékenységnapló-riasztását.</span><span class="sxs-lookup"><span data-stu-id="bd734-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="bd734-112">2. példa: Tevékenységnapló-riasztások lekérte az adott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="bd734-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="bd734-113">Ez a parancs felsorolja az adott erőforráscsoport tevékenységnapló-riasztását.</span><span class="sxs-lookup"><span data-stu-id="bd734-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="bd734-114">3. példa: Tevékenységnapló-riasztást kap.</span><span class="sxs-lookup"><span data-stu-id="bd734-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="bd734-115">Ez a parancs felsorolja az egyik (egyetlen elemet tartalmazó listát) tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="bd734-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="bd734-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd734-116">PARAMETERS</span></span>

### <span data-ttu-id="bd734-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd734-117">-DefaultProfile</span></span>
<span data-ttu-id="bd734-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bd734-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd734-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bd734-119">-Name</span></span>
<span data-ttu-id="bd734-120">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="bd734-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="bd734-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd734-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd734-122">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="bd734-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="bd734-123">Ha a név nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="bd734-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="bd734-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd734-124">CommonParameters</span></span>
<span data-ttu-id="bd734-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd734-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd734-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd734-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd734-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd734-127">INPUTS</span></span>

### <span data-ttu-id="bd734-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bd734-128">System.String</span></span>

## <span data-ttu-id="bd734-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd734-129">OUTPUTS</span></span>

### <span data-ttu-id="bd734-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="bd734-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="bd734-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd734-131">NOTES</span></span>

## <span data-ttu-id="bd734-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd734-132">RELATED LINKS</span></span>

[<span data-ttu-id="bd734-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bd734-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="bd734-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bd734-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="bd734-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="bd734-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="bd734-136">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="bd734-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="bd734-137">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="bd734-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
