---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: ca4229f5f882b1065c6f39b8c162bb91b90b835d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842062"
---
# <span data-ttu-id="e1266-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e1266-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="e1266-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1266-102">SYNOPSIS</span></span>
<span data-ttu-id="e1266-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="e1266-103">Gets action group(s).</span></span>

## <span data-ttu-id="e1266-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1266-104">SYNTAX</span></span>

### <span data-ttu-id="e1266-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1266-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1266-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e1266-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1266-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1266-107">DESCRIPTION</span></span>
<span data-ttu-id="e1266-108">A **Get-AzActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="e1266-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="e1266-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e1266-109">EXAMPLES</span></span>

### <span data-ttu-id="e1266-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="e1266-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="e1266-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="e1266-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="e1266-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="e1266-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="e1266-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="e1266-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="e1266-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1266-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="e1266-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="e1266-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="e1266-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1266-116">PARAMETERS</span></span>

### <span data-ttu-id="e1266-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1266-117">-DefaultProfile</span></span>
<span data-ttu-id="e1266-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e1266-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1266-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1266-119">-Name</span></span>
<span data-ttu-id="e1266-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e1266-120">The name of the action group.</span></span>

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

### <span data-ttu-id="e1266-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1266-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1266-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e1266-122">The resource group name</span></span>

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

### <span data-ttu-id="e1266-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1266-123">CommonParameters</span></span>
<span data-ttu-id="e1266-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1266-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1266-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e1266-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1266-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1266-126">INPUTS</span></span>

### <span data-ttu-id="e1266-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e1266-127">System.String</span></span>

## <span data-ttu-id="e1266-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1266-128">OUTPUTS</span></span>

### <span data-ttu-id="e1266-129">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="e1266-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="e1266-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1266-130">NOTES</span></span>

## <span data-ttu-id="e1266-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1266-131">RELATED LINKS</span></span>

<span data-ttu-id="e1266-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="e1266-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
