---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2f62b33b7a5a2224f54be765d03f72fc1667cec1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503675"
---
# <span data-ttu-id="94a65-101">Remove-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="94a65-101">Remove-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="94a65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94a65-102">SYNOPSIS</span></span>
<span data-ttu-id="94a65-103">Diagnosztikai beállítás eltávolítása az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="94a65-103">Remove a diagnostic setting for the a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94a65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94a65-104">SYNTAX</span></span>

```
Remove-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a65-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94a65-105">DESCRIPTION</span></span>
<span data-ttu-id="94a65-106">A **Remove-AzureRmDiagnosticSetting** parancsmag eltávolítja az adott erőforrás diagnosztikai beállítását.</span><span class="sxs-lookup"><span data-stu-id="94a65-106">The **Remove-AzureRmDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="94a65-107">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="94a65-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="94a65-108">Példák</span><span class="sxs-lookup"><span data-stu-id="94a65-108">EXAMPLES</span></span>

### <span data-ttu-id="94a65-109">1. példa: az alapértelmezett diagnosztikai beállítás (szolgáltatás) eltávolítása egy erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="94a65-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="94a65-110">Ez a parancs eltávolítja a Resource01 nevű erőforrás alapértelmezett diagnosztikai beállítását (szolgáltatást).</span><span class="sxs-lookup"><span data-stu-id="94a65-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="94a65-111">2. példa: az alapértelmezett diagnosztikai beállítás eltávolítása egy erőforrás megadott nevével</span><span class="sxs-lookup"><span data-stu-id="94a65-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzureRmDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="94a65-112">Ez a parancs eltávolítja a myDiagSetting nevű diagnosztikai beállítást az Resource01 nevű erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="94a65-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="94a65-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94a65-113">PARAMETERS</span></span>

### <span data-ttu-id="94a65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a65-114">-DefaultProfile</span></span>
<span data-ttu-id="94a65-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94a65-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a65-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94a65-116">-Name</span></span>
<span data-ttu-id="94a65-117">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="94a65-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="94a65-118">Ha nem adja meg a "szolgáltatás" hívás alapértelmezett hívását a korábbi API-ban, és ez a parancsmag csak a metrikák/naplók minden kategóriáját letiltja.</span><span class="sxs-lookup"><span data-stu-id="94a65-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

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

### <span data-ttu-id="94a65-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94a65-119">-ResourceId</span></span>
<span data-ttu-id="94a65-120">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="94a65-120">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="94a65-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94a65-121">-Confirm</span></span>
<span data-ttu-id="94a65-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94a65-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a65-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a65-123">-WhatIf</span></span>
<span data-ttu-id="94a65-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94a65-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94a65-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94a65-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a65-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a65-126">CommonParameters</span></span>
<span data-ttu-id="94a65-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94a65-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a65-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a65-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a65-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a65-129">INPUTS</span></span>

### <span data-ttu-id="94a65-130">System. String</span><span class="sxs-lookup"><span data-stu-id="94a65-130">System.String</span></span>

## <span data-ttu-id="94a65-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a65-131">OUTPUTS</span></span>

### <span data-ttu-id="94a65-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94a65-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="94a65-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94a65-133">NOTES</span></span>

## <span data-ttu-id="94a65-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94a65-134">RELATED LINKS</span></span>

<span data-ttu-id="94a65-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="94a65-135">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)</span></span>
