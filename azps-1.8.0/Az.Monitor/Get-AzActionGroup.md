---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: c77585666187e9b55c14de1699140ca2f5cc6288
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835109"
---
# <span data-ttu-id="7ec97-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="7ec97-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="7ec97-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ec97-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec97-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="7ec97-103">Gets action group(s).</span></span>

## <span data-ttu-id="7ec97-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ec97-104">SYNTAX</span></span>

### <span data-ttu-id="7ec97-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ec97-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ec97-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7ec97-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ec97-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ec97-107">DESCRIPTION</span></span>
<span data-ttu-id="7ec97-108">A **Get-AzActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="7ec97-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="7ec97-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7ec97-109">EXAMPLES</span></span>

### <span data-ttu-id="7ec97-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="7ec97-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="7ec97-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="7ec97-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="7ec97-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="7ec97-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="7ec97-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="7ec97-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="7ec97-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="7ec97-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="7ec97-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="7ec97-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="7ec97-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ec97-116">PARAMETERS</span></span>

### <span data-ttu-id="7ec97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec97-117">-DefaultProfile</span></span>
<span data-ttu-id="7ec97-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ec97-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ec97-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ec97-119">-Name</span></span>
<span data-ttu-id="7ec97-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="7ec97-120">The name of the action group.</span></span>

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

### <span data-ttu-id="7ec97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec97-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ec97-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7ec97-122">The resource group name</span></span>

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

### <span data-ttu-id="7ec97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec97-123">CommonParameters</span></span>
<span data-ttu-id="7ec97-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ec97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec97-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec97-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec97-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec97-126">INPUTS</span></span>

### <span data-ttu-id="7ec97-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec97-127">System.String</span></span>

## <span data-ttu-id="7ec97-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec97-128">OUTPUTS</span></span>

### <span data-ttu-id="7ec97-129">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="7ec97-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="7ec97-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ec97-130">NOTES</span></span>

## <span data-ttu-id="7ec97-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ec97-131">RELATED LINKS</span></span>

<span data-ttu-id="7ec97-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="7ec97-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
