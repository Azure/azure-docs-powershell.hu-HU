---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 93112c8e7518ac23b23e5b1bb6c18109481495dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403153"
---
# <span data-ttu-id="2b43f-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2b43f-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="2b43f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b43f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b43f-103">Egy vagy több tevékenységnapló-riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="2b43f-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2b43f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b43f-104">SYNTAX</span></span>

### <span data-ttu-id="2b43f-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b43f-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b43f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b43f-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b43f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b43f-107">DESCRIPTION</span></span>
<span data-ttu-id="2b43f-108">A **Get-AzActivityLogAlert** parancsmag egy vagy több tevékenységnapló-riasztási erőforrást kap.</span><span class="sxs-lookup"><span data-stu-id="2b43f-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2b43f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b43f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b43f-110">1. példa: Tevékenységnapló-riasztások lekérte előfizetésazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="2b43f-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="2b43f-111">Ez a parancs felsorolja az aktuális előfizetés összes tevékenységnapló-riasztását.</span><span class="sxs-lookup"><span data-stu-id="2b43f-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="2b43f-112">2. példa: Tevékenységnapló-riasztások lekérte az adott erőforráscsoporthoz</span><span class="sxs-lookup"><span data-stu-id="2b43f-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="2b43f-113">Ez a parancs felsorolja az adott erőforráscsoport tevékenységnapló-riasztását.</span><span class="sxs-lookup"><span data-stu-id="2b43f-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="2b43f-114">3. példa: Tevékenységnapló-riasztást kap.</span><span class="sxs-lookup"><span data-stu-id="2b43f-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="2b43f-115">Ez a parancs felsorolja az egyik (egyetlen elemet tartalmazó listát) tevékenységnapló-riasztást.</span><span class="sxs-lookup"><span data-stu-id="2b43f-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="2b43f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b43f-116">PARAMETERS</span></span>

### <span data-ttu-id="2b43f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b43f-117">-DefaultProfile</span></span>
<span data-ttu-id="2b43f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b43f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b43f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2b43f-119">-Name</span></span>
<span data-ttu-id="2b43f-120">A tevékenységnapló-riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="2b43f-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="2b43f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b43f-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b43f-122">Annak az erőforráscsoportnak a neve, amelyben a riasztási erőforrás létezik.</span><span class="sxs-lookup"><span data-stu-id="2b43f-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="2b43f-123">Ha a Név értéke nem null vagy üres, a paraméternek tartalmaznia kell és nem üres karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="2b43f-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="2b43f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b43f-124">CommonParameters</span></span>
<span data-ttu-id="2b43f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b43f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b43f-126">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b43f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b43f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b43f-127">INPUTS</span></span>

### <span data-ttu-id="2b43f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2b43f-128">System.String</span></span>

## <span data-ttu-id="2b43f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b43f-129">OUTPUTS</span></span>

### <span data-ttu-id="2b43f-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2b43f-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2b43f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b43f-131">NOTES</span></span>

## <span data-ttu-id="2b43f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b43f-132">RELATED LINKS</span></span>

[<span data-ttu-id="2b43f-133">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2b43f-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2b43f-134">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2b43f-134">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2b43f-135">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2b43f-135">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
