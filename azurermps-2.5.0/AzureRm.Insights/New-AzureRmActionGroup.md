---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848290"
---
# <span data-ttu-id="12cb7-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="12cb7-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="12cb7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="12cb7-103">Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="12cb7-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12cb7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12cb7-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12cb7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="12cb7-106">A **New-AzureRmActionGroup** parancsmag létrehoz egy műveleti csoport hivatkozási objektumát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="12cb7-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="12cb7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="12cb7-107">EXAMPLES</span></span>

### <span data-ttu-id="12cb7-108">Példa 1: Művelettípus-viszonyítási objektum létrehozása a memóriában</span><span class="sxs-lookup"><span data-stu-id="12cb7-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="12cb7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12cb7-109">PARAMETERS</span></span>

### <span data-ttu-id="12cb7-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="12cb7-110">-ActionGroupId</span></span>
<span data-ttu-id="12cb7-111">A műveleti csoport azonosítója/neve.</span><span class="sxs-lookup"><span data-stu-id="12cb7-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12cb7-112">-DefaultProfile</span></span>
<span data-ttu-id="12cb7-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="12cb7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12cb7-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="12cb7-114">-WebhookProperty</span></span>
<span data-ttu-id="12cb7-115">A műveleti csoport webhook-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="12cb7-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12cb7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12cb7-116">CommonParameters</span></span>
<span data-ttu-id="12cb7-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12cb7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12cb7-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12cb7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12cb7-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cb7-119">INPUTS</span></span>

### <span data-ttu-id="12cb7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="12cb7-120">System.String</span></span>

### <span data-ttu-id="12cb7-121">System. Collections. Generic. Dictionary ' 2 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089], [System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="12cb7-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="12cb7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12cb7-122">OUTPUTS</span></span>

### <span data-ttu-id="12cb7-123">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="12cb7-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="12cb7-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12cb7-124">NOTES</span></span>

## <span data-ttu-id="12cb7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12cb7-125">RELATED LINKS</span></span>

[<span data-ttu-id="12cb7-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12cb7-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12cb7-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12cb7-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12cb7-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12cb7-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12cb7-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12cb7-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12cb7-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12cb7-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="12cb7-131">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="12cb7-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

