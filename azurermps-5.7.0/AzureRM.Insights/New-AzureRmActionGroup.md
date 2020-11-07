---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672644"
---
# <span data-ttu-id="a19c6-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a19c6-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="a19c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a19c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a19c6-103">Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="a19c6-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a19c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a19c6-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a19c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a19c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a19c6-106">A **New-AzureRmActionGroup** parancsmag létrehoz egy műveleti csoport hivatkozási objektumát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="a19c6-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="a19c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a19c6-107">EXAMPLES</span></span>

### <span data-ttu-id="a19c6-108">Példa 1: Művelettípus-viszonyítási objektum létrehozása a memóriában</span><span class="sxs-lookup"><span data-stu-id="a19c6-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="a19c6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a19c6-109">PARAMETERS</span></span>

### <span data-ttu-id="a19c6-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="a19c6-110">-ActionGroupId</span></span>
<span data-ttu-id="a19c6-111">A műveleti csoport azonosítója/neve.</span><span class="sxs-lookup"><span data-stu-id="a19c6-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a19c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19c6-112">-DefaultProfile</span></span>
<span data-ttu-id="a19c6-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a19c6-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a19c6-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="a19c6-114">-WebhookProperty</span></span>
<span data-ttu-id="a19c6-115">A műveleti csoport webhook-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="a19c6-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="a19c6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19c6-116">CommonParameters</span></span>
<span data-ttu-id="a19c6-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a19c6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19c6-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19c6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19c6-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a19c6-119">INPUTS</span></span>

### <span data-ttu-id="a19c6-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="a19c6-120">None</span></span>
<span data-ttu-id="a19c6-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a19c6-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a19c6-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a19c6-122">OUTPUTS</span></span>

### <span data-ttu-id="a19c6-123">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="a19c6-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="a19c6-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a19c6-124">NOTES</span></span>

## <span data-ttu-id="a19c6-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a19c6-125">RELATED LINKS</span></span>

[<span data-ttu-id="a19c6-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a19c6-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a19c6-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a19c6-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a19c6-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a19c6-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a19c6-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a19c6-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a19c6-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a19c6-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a19c6-131">Új – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a19c6-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

