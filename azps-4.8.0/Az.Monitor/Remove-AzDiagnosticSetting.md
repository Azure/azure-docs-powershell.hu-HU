---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024690"
---
# <span data-ttu-id="0fed8-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="0fed8-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="0fed8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0fed8-102">SYNOPSIS</span></span>
<span data-ttu-id="0fed8-103">Diagnosztikai beállítás eltávolítása az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="0fed8-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="0fed8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0fed8-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fed8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0fed8-105">DESCRIPTION</span></span>
<span data-ttu-id="0fed8-106">A **Remove-AzDiagnosticSetting** parancsmag eltávolítja az adott erőforrás diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="0fed8-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="0fed8-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="0fed8-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0fed8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="0fed8-108">EXAMPLES</span></span>

### <span data-ttu-id="0fed8-109">1. példa: az alapértelmezett diagnosztikai beállítás (szolgáltatás) eltávolítása egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="0fed8-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="0fed8-110">Ez a parancs eltávolítja a Resource01 nevű erőforrás alapértelmezett diagnosztikai beállítását (szolgáltatást).</span><span class="sxs-lookup"><span data-stu-id="0fed8-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="0fed8-111">2. példa: az alapértelmezett diagnosztikai beállítás eltávolítása egy erőforrás megadott nevével</span><span class="sxs-lookup"><span data-stu-id="0fed8-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="0fed8-112">Ez a parancs eltávolítja a myDiagSetting nevű diagnosztikai beállítást az Resource01 nevű erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="0fed8-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="0fed8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0fed8-113">PARAMETERS</span></span>

### <span data-ttu-id="0fed8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fed8-114">-DefaultProfile</span></span>
<span data-ttu-id="0fed8-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fed8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fed8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0fed8-116">-Name</span></span>
<span data-ttu-id="0fed8-117">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="0fed8-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="0fed8-118">Ha nem adja meg a "szolgáltatás" hívás alapértelmezett hívását a korábbi API-ban, és ez a parancsmag csak a metrikák/naplók minden kategóriáját letiltja.</span><span class="sxs-lookup"><span data-stu-id="0fed8-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="0fed8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fed8-119">-ResourceId</span></span>
<span data-ttu-id="0fed8-120">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0fed8-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="0fed8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0fed8-121">-Confirm</span></span>
<span data-ttu-id="0fed8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0fed8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fed8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fed8-123">-WhatIf</span></span>
<span data-ttu-id="0fed8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0fed8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fed8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fed8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fed8-126">CommonParameters</span></span>
<span data-ttu-id="0fed8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0fed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fed8-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0fed8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fed8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fed8-129">INPUTS</span></span>

### <span data-ttu-id="0fed8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0fed8-130">System.String</span></span>

## <span data-ttu-id="0fed8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fed8-131">OUTPUTS</span></span>

### <span data-ttu-id="0fed8-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0fed8-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0fed8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0fed8-133">NOTES</span></span>

## <span data-ttu-id="0fed8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fed8-134">RELATED LINKS</span></span>

<span data-ttu-id="0fed8-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="0fed8-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>
