---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementBackend.md
ms.openlocfilehash: ef00a5140dc25065c05494211721c5773a9b5243
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492076"
---
# <span data-ttu-id="96312-101">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="96312-101">Remove-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="96312-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96312-102">SYNOPSIS</span></span>
<span data-ttu-id="96312-103">A backend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="96312-103">Removes a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96312-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96312-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96312-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96312-105">DESCRIPTION</span></span>
<span data-ttu-id="96312-106">Eltávolítja az azonosító által az API-menedzsment által megadott hátteret.</span><span class="sxs-lookup"><span data-stu-id="96312-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="96312-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96312-107">EXAMPLES</span></span>

### <span data-ttu-id="96312-108">1. példa: a backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="96312-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="96312-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96312-109">PARAMETERS</span></span>

### <span data-ttu-id="96312-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="96312-110">-BackendId</span></span>
<span data-ttu-id="96312-111">A meglévő backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="96312-111">Identifier of existing backend.</span></span>
<span data-ttu-id="96312-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96312-112">This parameter is required.</span></span>

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

### <span data-ttu-id="96312-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96312-113">-Context</span></span>
<span data-ttu-id="96312-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="96312-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="96312-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="96312-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96312-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96312-116">-DefaultProfile</span></span>
<span data-ttu-id="96312-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96312-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96312-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96312-118">-PassThru</span></span>
<span data-ttu-id="96312-119">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="96312-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="96312-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="96312-120">This parameter is optional.</span></span>
<span data-ttu-id="96312-121">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="96312-121">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96312-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96312-122">-Confirm</span></span>
<span data-ttu-id="96312-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96312-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96312-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96312-124">-WhatIf</span></span>
<span data-ttu-id="96312-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96312-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96312-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96312-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96312-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96312-127">CommonParameters</span></span>
<span data-ttu-id="96312-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96312-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96312-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96312-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96312-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96312-130">INPUTS</span></span>

### <span data-ttu-id="96312-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="96312-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="96312-132">System. String</span><span class="sxs-lookup"><span data-stu-id="96312-132">System.String</span></span>

### <span data-ttu-id="96312-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="96312-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="96312-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96312-134">OUTPUTS</span></span>

### <span data-ttu-id="96312-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96312-135">System.Boolean</span></span>

## <span data-ttu-id="96312-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96312-136">NOTES</span></span>

## <span data-ttu-id="96312-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96312-137">RELATED LINKS</span></span>

[<span data-ttu-id="96312-138">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="96312-138">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="96312-139">Új – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="96312-139">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="96312-140">Új – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="96312-140">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="96312-141">Új – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="96312-141">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="96312-142">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="96312-142">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)
