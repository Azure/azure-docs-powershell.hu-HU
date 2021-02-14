---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203514"
---
# <span data-ttu-id="7dd26-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="7dd26-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="7dd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dd26-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd26-103">Műveletcsoport(ak) lekérte.</span><span class="sxs-lookup"><span data-stu-id="7dd26-103">Gets action group(s).</span></span>

## <span data-ttu-id="7dd26-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7dd26-104">SYNTAX</span></span>

### <span data-ttu-id="7dd26-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7dd26-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dd26-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7dd26-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dd26-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7dd26-107">DESCRIPTION</span></span>
<span data-ttu-id="7dd26-108">A **Get-AzActionGroup** parancsmag egy vagy több műveletcsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="7dd26-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="7dd26-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7dd26-109">EXAMPLES</span></span>

### <span data-ttu-id="7dd26-110">1. példa: Műveletcsoport lekérte előfizetésazonosító szerint</span><span class="sxs-lookup"><span data-stu-id="7dd26-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="7dd26-111">Ez a parancs felsorolja az aktuális előfizetés összes műveletcsoportját.</span><span class="sxs-lookup"><span data-stu-id="7dd26-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="7dd26-112">2. példa: Az adott erőforráscsoporthoz szükséges műveletcsoportok lekérte</span><span class="sxs-lookup"><span data-stu-id="7dd26-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="7dd26-113">Ez a parancs felsorolja az adott erőforráscsoporthoz szükséges műveletcsoportokat.</span><span class="sxs-lookup"><span data-stu-id="7dd26-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="7dd26-114">3. példa: Műveletcsoport lekérte.</span><span class="sxs-lookup"><span data-stu-id="7dd26-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="7dd26-115">Ez a parancs felsorol egy (egyetlen elemet tartalmazó listát) műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="7dd26-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="7dd26-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dd26-116">PARAMETERS</span></span>

### <span data-ttu-id="7dd26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd26-117">-DefaultProfile</span></span>
<span data-ttu-id="7dd26-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7dd26-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dd26-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7dd26-119">-Name</span></span>
<span data-ttu-id="7dd26-120">A műveletcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7dd26-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd26-121">-ResourceGroupName</span></span>
<span data-ttu-id="7dd26-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7dd26-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd26-123">CommonParameters</span></span>
<span data-ttu-id="7dd26-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd26-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7dd26-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd26-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dd26-126">INPUTS</span></span>

### <span data-ttu-id="7dd26-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7dd26-127">System.String</span></span>

## <span data-ttu-id="7dd26-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dd26-128">OUTPUTS</span></span>

### <span data-ttu-id="7dd26-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="7dd26-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="7dd26-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7dd26-130">NOTES</span></span>

## <span data-ttu-id="7dd26-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dd26-131">RELATED LINKS</span></span>

<span data-ttu-id="7dd26-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="7dd26-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
