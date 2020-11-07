---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 1377e1fe5f96754f4b20858cc1930039246bd8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837457"
---
# <span data-ttu-id="122ce-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="122ce-101">New-AzActionGroup</span></span>

## <span data-ttu-id="122ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="122ce-102">SYNOPSIS</span></span>
<span data-ttu-id="122ce-103">Egy ActionGroup-viszonyítási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="122ce-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="122ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="122ce-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="122ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="122ce-105">DESCRIPTION</span></span>
<span data-ttu-id="122ce-106">A **New-AzActionGroup** parancsmag létrehoz egy műveleti csoport hivatkozási objektumát a memóriában.</span><span class="sxs-lookup"><span data-stu-id="122ce-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="122ce-107">Példák</span><span class="sxs-lookup"><span data-stu-id="122ce-107">EXAMPLES</span></span>

### <span data-ttu-id="122ce-108">Példa 1: Művelettípus-viszonyítási objektum létrehozása a memóriában</span><span class="sxs-lookup"><span data-stu-id="122ce-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="122ce-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="122ce-109">PARAMETERS</span></span>

### <span data-ttu-id="122ce-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="122ce-110">-ActionGroupId</span></span>
<span data-ttu-id="122ce-111">A műveleti csoport azonosítója/neve.</span><span class="sxs-lookup"><span data-stu-id="122ce-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="122ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="122ce-112">-DefaultProfile</span></span>
<span data-ttu-id="122ce-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="122ce-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="122ce-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="122ce-114">-WebhookProperty</span></span>
<span data-ttu-id="122ce-115">A műveleti csoport webhook-tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="122ce-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="122ce-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="122ce-116">CommonParameters</span></span>
<span data-ttu-id="122ce-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="122ce-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="122ce-118">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="122ce-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="122ce-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="122ce-119">INPUTS</span></span>

### <span data-ttu-id="122ce-120">System. String</span><span class="sxs-lookup"><span data-stu-id="122ce-120">System.String</span></span>

### <span data-ttu-id="122ce-121">System. Collections. Generic. Dictionary ' 2 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e], [System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="122ce-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="122ce-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="122ce-122">OUTPUTS</span></span>

### <span data-ttu-id="122ce-123">Microsoft. Azure. Management. monitor. Management. models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="122ce-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="122ce-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="122ce-124">NOTES</span></span>

## <span data-ttu-id="122ce-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="122ce-125">RELATED LINKS</span></span>

[<span data-ttu-id="122ce-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="122ce-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="122ce-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="122ce-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="122ce-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="122ce-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="122ce-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="122ce-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="122ce-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="122ce-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="122ce-131">Új – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="122ce-131">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

