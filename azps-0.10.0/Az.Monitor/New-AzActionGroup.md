---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 9d29240e4be9039e75491ede7d835ecba99aa2d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842013"
---
# <span data-ttu-id="31f00-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="31f00-101">New-AzActionGroup</span></span>

## <span data-ttu-id="31f00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31f00-102">SYNOPSIS</span></span>
<span data-ttu-id="31f00-103">Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="31f00-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="31f00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31f00-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f00-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31f00-105">DESCRIPTION</span></span>
<span data-ttu-id="31f00-106">A **New-AzActionGroup** parancsmag létrehoz egy műveleti csoport hivatkozási objektumát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="31f00-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="31f00-107">Példák</span><span class="sxs-lookup"><span data-stu-id="31f00-107">EXAMPLES</span></span>

### <span data-ttu-id="31f00-108">Példa 1: Művelettípus-viszonyítási objektum létrehozása a memóriában</span><span class="sxs-lookup"><span data-stu-id="31f00-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="31f00-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31f00-109">PARAMETERS</span></span>

### <span data-ttu-id="31f00-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="31f00-110">-ActionGroupId</span></span>
<span data-ttu-id="31f00-111">A műveleti csoport azonosítója/neve.</span><span class="sxs-lookup"><span data-stu-id="31f00-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="31f00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f00-112">-DefaultProfile</span></span>
<span data-ttu-id="31f00-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="31f00-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31f00-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="31f00-114">-WebhookProperty</span></span>
<span data-ttu-id="31f00-115">A műveleti csoport webhook-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="31f00-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="31f00-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f00-116">CommonParameters</span></span>
<span data-ttu-id="31f00-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31f00-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f00-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="31f00-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f00-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31f00-119">INPUTS</span></span>

### <span data-ttu-id="31f00-120">System. String</span><span class="sxs-lookup"><span data-stu-id="31f00-120">System.String</span></span>

### <span data-ttu-id="31f00-121">System. Collections. Generic. Dictionary ' 2 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e], [System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="31f00-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="31f00-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31f00-122">OUTPUTS</span></span>

### <span data-ttu-id="31f00-123">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="31f00-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="31f00-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31f00-124">NOTES</span></span>

## <span data-ttu-id="31f00-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31f00-125">RELATED LINKS</span></span>

[<span data-ttu-id="31f00-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="31f00-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="31f00-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="31f00-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="31f00-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="31f00-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="31f00-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="31f00-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="31f00-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="31f00-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="31f00-131">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="31f00-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

