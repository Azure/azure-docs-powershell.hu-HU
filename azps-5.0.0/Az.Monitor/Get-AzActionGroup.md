---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195762"
---
# <span data-ttu-id="e321b-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e321b-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="e321b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e321b-102">SYNOPSIS</span></span>
<span data-ttu-id="e321b-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="e321b-103">Gets action group(s).</span></span>

## <span data-ttu-id="e321b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e321b-104">SYNTAX</span></span>

### <span data-ttu-id="e321b-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e321b-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e321b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e321b-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e321b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e321b-107">DESCRIPTION</span></span>
<span data-ttu-id="e321b-108">A **Get-AzActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="e321b-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="e321b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e321b-109">EXAMPLES</span></span>

### <span data-ttu-id="e321b-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="e321b-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="e321b-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="e321b-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="e321b-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e321b-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="e321b-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="e321b-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="e321b-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e321b-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="e321b-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="e321b-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="e321b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e321b-116">PARAMETERS</span></span>

### <span data-ttu-id="e321b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e321b-117">-DefaultProfile</span></span>
<span data-ttu-id="e321b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e321b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e321b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e321b-119">-Name</span></span>
<span data-ttu-id="e321b-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e321b-120">The name of the action group.</span></span>

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

### <span data-ttu-id="e321b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e321b-121">-ResourceGroupName</span></span>
<span data-ttu-id="e321b-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e321b-122">The resource group name</span></span>

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

### <span data-ttu-id="e321b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e321b-123">CommonParameters</span></span>
<span data-ttu-id="e321b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e321b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e321b-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e321b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e321b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e321b-126">INPUTS</span></span>

### <span data-ttu-id="e321b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e321b-127">System.String</span></span>

## <span data-ttu-id="e321b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e321b-128">OUTPUTS</span></span>

### <span data-ttu-id="e321b-129">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e321b-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="e321b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e321b-130">NOTES</span></span>

## <span data-ttu-id="e321b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e321b-131">RELATED LINKS</span></span>

<span data-ttu-id="e321b-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e321b-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
