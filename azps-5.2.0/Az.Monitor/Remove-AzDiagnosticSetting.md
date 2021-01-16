---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328561"
---
# <span data-ttu-id="ef062-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="ef062-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="ef062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef062-102">SYNOPSIS</span></span>
<span data-ttu-id="ef062-103">Távolítsa el az erőforrás diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="ef062-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="ef062-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ef062-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef062-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ef062-105">DESCRIPTION</span></span>
<span data-ttu-id="ef062-106">A **Remove-AzDiagnosticSetting** parancsmag eltávolítja az adott erőforrás diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="ef062-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="ef062-107">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="ef062-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ef062-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ef062-108">EXAMPLES</span></span>

### <span data-ttu-id="ef062-109">1. példa: Erőforrás alapértelmezett diagnosztikai beállításának (szolgáltatásának) eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef062-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="ef062-110">Ez a parancs eltávolítja az Erőforrás01 nevű erőforrás alapértelmezett diagnosztikai beállítását (szolgáltatását).</span><span class="sxs-lookup"><span data-stu-id="ef062-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="ef062-111">2. példa: Az erőforráshoz megadott névvel megadott alapértelmezett diagnosztikai beállítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ef062-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="ef062-112">Ez a parancs eltávolítja az Erőforrás01 nevű erőforrás myDiagSetting nevű diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="ef062-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="ef062-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef062-113">PARAMETERS</span></span>

### <span data-ttu-id="ef062-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef062-114">-DefaultProfile</span></span>
<span data-ttu-id="ef062-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ef062-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef062-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef062-116">-Name</span></span>
<span data-ttu-id="ef062-117">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="ef062-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="ef062-118">Ha a hívás alapértelmezés szerint nem "szolgáltatás" lesz, mint az előző API-ban, és ez a parancsmag csak a metrikák/naplók kategóriáit tiltja le.</span><span class="sxs-lookup"><span data-stu-id="ef062-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef062-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef062-119">-ResourceId</span></span>
<span data-ttu-id="ef062-120">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ef062-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="ef062-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef062-121">-Confirm</span></span>
<span data-ttu-id="ef062-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ef062-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef062-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef062-123">-WhatIf</span></span>
<span data-ttu-id="ef062-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ef062-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef062-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef062-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef062-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef062-126">CommonParameters</span></span>
<span data-ttu-id="ef062-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef062-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef062-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef062-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef062-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef062-129">INPUTS</span></span>

### <span data-ttu-id="ef062-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ef062-130">System.String</span></span>

## <span data-ttu-id="ef062-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef062-131">OUTPUTS</span></span>

### <span data-ttu-id="ef062-132">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ef062-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="ef062-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ef062-133">NOTES</span></span>

## <span data-ttu-id="ef062-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef062-134">RELATED LINKS</span></span>

<span data-ttu-id="ef062-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="ef062-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
