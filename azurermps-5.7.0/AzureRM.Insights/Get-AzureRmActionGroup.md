---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActionGroup.md
ms.openlocfilehash: 08785d6fe4afe918ca593eeff7ee7aa9cfbfe578
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678986"
---
# <span data-ttu-id="dedcb-101">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="dedcb-101">Get-AzureRmActionGroup</span></span>

## <span data-ttu-id="dedcb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dedcb-102">SYNOPSIS</span></span>
<span data-ttu-id="dedcb-103">A műveleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="dedcb-103">Gets action group(s).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dedcb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dedcb-104">SYNTAX</span></span>

### <span data-ttu-id="dedcb-105">BySubscriptionOrResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dedcb-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dedcb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dedcb-106">ByName</span></span>
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dedcb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dedcb-107">DESCRIPTION</span></span>
<span data-ttu-id="dedcb-108">A **Get-AzureRmActionGroup** parancsmag egy vagy több műveleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="dedcb-108">The **Get-AzureRmActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="dedcb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dedcb-109">EXAMPLES</span></span>

### <span data-ttu-id="dedcb-110">1. példa: műveletkérő csoport beszerzése előfizetés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="dedcb-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzureRmActionGroup
```

<span data-ttu-id="dedcb-111">Ez a parancs felsorolja az aktuális előfizetéshez tartozó összes Művelettípus-csoportot.</span><span class="sxs-lookup"><span data-stu-id="dedcb-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="dedcb-112">2. példa: az adott erőforráscsoport műveleti csoportjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="dedcb-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="dedcb-113">Ez a parancs megjeleníti a megadott erőforráscsoport műveleti csoportját.</span><span class="sxs-lookup"><span data-stu-id="dedcb-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="dedcb-114">3. példa: művelet csoportjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="dedcb-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="dedcb-115">Ez a parancs egy (egyetlen elemből álló) műveleti csoporttal sorolja fel a listát.</span><span class="sxs-lookup"><span data-stu-id="dedcb-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="dedcb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dedcb-116">PARAMETERS</span></span>

### <span data-ttu-id="dedcb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedcb-117">-DefaultProfile</span></span>
<span data-ttu-id="dedcb-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dedcb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dedcb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dedcb-119">-Name</span></span>
<span data-ttu-id="dedcb-120">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="dedcb-120">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedcb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedcb-121">-ResourceGroupName</span></span>
<span data-ttu-id="dedcb-122">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="dedcb-122">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dedcb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedcb-123">CommonParameters</span></span>
<span data-ttu-id="dedcb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dedcb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedcb-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dedcb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedcb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedcb-126">INPUTS</span></span>

### <span data-ttu-id="dedcb-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="dedcb-127">None</span></span>

## <span data-ttu-id="dedcb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dedcb-128">OUTPUTS</span></span>

### <span data-ttu-id="dedcb-129"><System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. detekintést. OutputClasses. PSActionGroupResource]</span><span class="sxs-lookup"><span data-stu-id="dedcb-129"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource]</span></span>

### <span data-ttu-id="dedcb-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="dedcb-130">None</span></span>

## <span data-ttu-id="dedcb-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dedcb-131">NOTES</span></span>

## <span data-ttu-id="dedcb-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dedcb-132">RELATED LINKS</span></span>

<span data-ttu-id="dedcb-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="dedcb-133">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
