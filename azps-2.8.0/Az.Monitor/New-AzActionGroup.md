---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 47ab8423de29a1cdfeb7edb268560bb28cfc8ac7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411398"
---
# <span data-ttu-id="c597c-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c597c-101">New-AzActionGroup</span></span>

## <span data-ttu-id="c597c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c597c-102">SYNOPSIS</span></span>
<span data-ttu-id="c597c-103">Műveletcsoport-hivatkozási objektumot hoz létre a memóriában.</span><span class="sxs-lookup"><span data-stu-id="c597c-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="c597c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c597c-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c597c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c597c-105">DESCRIPTION</span></span>
<span data-ttu-id="c597c-106">A **New-AzActionGroup** parancsmag létrehoz egy műveletcsoport-hivatkozási objektumot a memóriában.</span><span class="sxs-lookup"><span data-stu-id="c597c-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="c597c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c597c-107">EXAMPLES</span></span>

### <span data-ttu-id="c597c-108">1. példa: Műveletcsoport-hivatkozási objektum létrehozása a memóriában</span><span class="sxs-lookup"><span data-stu-id="c597c-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="c597c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c597c-109">PARAMETERS</span></span>

### <span data-ttu-id="c597c-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c597c-110">-ActionGroupId</span></span>
<span data-ttu-id="c597c-111">A műveletcsoport azonosítója/neve.</span><span class="sxs-lookup"><span data-stu-id="c597c-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="c597c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c597c-112">-DefaultProfile</span></span>
<span data-ttu-id="c597c-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c597c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c597c-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="c597c-114">-WebhookProperty</span></span>
<span data-ttu-id="c597c-115">A műveletcsoport webhook tulajdonságai</span><span class="sxs-lookup"><span data-stu-id="c597c-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="c597c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c597c-116">CommonParameters</span></span>
<span data-ttu-id="c597c-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c597c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c597c-118">További információt a [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c597c-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c597c-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c597c-119">INPUTS</span></span>

### <span data-ttu-id="c597c-120">System.String</span><span class="sxs-lookup"><span data-stu-id="c597c-120">System.String</span></span>

### <span data-ttu-id="c597c-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c597c-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c597c-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c597c-122">OUTPUTS</span></span>

### <span data-ttu-id="c597c-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="c597c-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="c597c-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c597c-124">NOTES</span></span>

## <span data-ttu-id="c597c-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c597c-125">RELATED LINKS</span></span>

[<span data-ttu-id="c597c-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c597c-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c597c-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c597c-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="c597c-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c597c-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="c597c-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c597c-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="c597c-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c597c-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



