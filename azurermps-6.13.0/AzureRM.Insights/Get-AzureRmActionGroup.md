---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 002847ae580e3e3c5d5b44e05ebc1633e4e1574b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672723"
---
# <span data-ttu-id="dec94-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="dec94-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="dec94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dec94-102">SYNOPSIS</span></span>
<span data-ttu-id="dec94-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="dec94-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dec94-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dec94-104">SYNTAX</span></span>

### <span data-ttu-id="dec94-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dec94-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dec94-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dec94-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dec94-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dec94-107">DESCRIPTION</span></span>
<span data-ttu-id="dec94-108">A **Get-AzureRmActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="dec94-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="dec94-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dec94-109">EXAMPLES</span></span>

### <span data-ttu-id="dec94-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="dec94-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="dec94-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="dec94-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="dec94-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="dec94-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="dec94-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="dec94-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="dec94-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dec94-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="dec94-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="dec94-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="dec94-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dec94-116">PARAMETERS</span></span>

### <span data-ttu-id="dec94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dec94-117">-DefaultProfile</span></span>
<span data-ttu-id="dec94-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dec94-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dec94-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dec94-119">-Name</span></span>
<span data-ttu-id="dec94-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dec94-120">The name of the action group.</span></span>

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

### <span data-ttu-id="dec94-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dec94-121">-ResourceGroupName</span></span>
<span data-ttu-id="dec94-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dec94-122">The resource group name</span></span>

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

### <span data-ttu-id="dec94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dec94-123">CommonParameters</span></span>
<span data-ttu-id="dec94-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dec94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dec94-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dec94-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dec94-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dec94-126">INPUTS</span></span>

### <span data-ttu-id="dec94-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dec94-127">System.String</span></span>

## <span data-ttu-id="dec94-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dec94-128">OUTPUTS</span></span>

### <span data-ttu-id="dec94-129">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="dec94-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="dec94-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dec94-130">NOTES</span></span>

## <span data-ttu-id="dec94-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dec94-131">RELATED LINKS</span></span>

<span data-ttu-id="dec94-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="dec94-132">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
