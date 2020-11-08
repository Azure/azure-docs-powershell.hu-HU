---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: c297198a1e49b93d498c136d1cb099d2068d24db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94015006"
---
# <span data-ttu-id="df394-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="df394-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="df394-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df394-102">SYNOPSIS</span></span>
<span data-ttu-id="df394-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="df394-103">Gets action group(s).</span></span>

## <span data-ttu-id="df394-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df394-104">SYNTAX</span></span>

### <span data-ttu-id="df394-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df394-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df394-106">ByName</span><span class="sxs-lookup"><span data-stu-id="df394-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df394-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="df394-107">DESCRIPTION</span></span>
<span data-ttu-id="df394-108">A **Get-AzActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="df394-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="df394-109">Példák</span><span class="sxs-lookup"><span data-stu-id="df394-109">EXAMPLES</span></span>

### <span data-ttu-id="df394-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="df394-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="df394-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="df394-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="df394-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="df394-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="df394-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="df394-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="df394-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="df394-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="df394-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="df394-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="df394-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df394-116">PARAMETERS</span></span>

### <span data-ttu-id="df394-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df394-117">-DefaultProfile</span></span>
<span data-ttu-id="df394-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df394-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df394-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df394-119">-Name</span></span>
<span data-ttu-id="df394-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="df394-120">The name of the action group.</span></span>

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

### <span data-ttu-id="df394-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df394-121">-ResourceGroupName</span></span>
<span data-ttu-id="df394-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="df394-122">The resource group name</span></span>

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

### <span data-ttu-id="df394-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df394-123">CommonParameters</span></span>
<span data-ttu-id="df394-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df394-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df394-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="df394-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df394-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df394-126">INPUTS</span></span>

### <span data-ttu-id="df394-127">System. String</span><span class="sxs-lookup"><span data-stu-id="df394-127">System.String</span></span>

## <span data-ttu-id="df394-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df394-128">OUTPUTS</span></span>

### <span data-ttu-id="df394-129">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="df394-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="df394-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df394-130">NOTES</span></span>

## <span data-ttu-id="df394-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df394-131">RELATED LINKS</span></span>

<span data-ttu-id="df394-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="df394-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
