---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 3a725bf8dedec948277fac69be029375c3ab91a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671668"
---
# <span data-ttu-id="5a3ef-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5a3ef-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="5a3ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5a3ef-103">A backend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-103">Removes a Backend.</span></span>

## <span data-ttu-id="5a3ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a3ef-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a3ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="5a3ef-106">Eltávolítja az azonosító által az API-menedzsment által megadott hátteret.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="5a3ef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5a3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="5a3ef-108">1. példa: a backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="5a3ef-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="5a3ef-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a3ef-109">PARAMETERS</span></span>

### <span data-ttu-id="5a3ef-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="5a3ef-110">-BackendId</span></span>
<span data-ttu-id="5a3ef-111">A meglévő backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-111">Identifier of existing backend.</span></span>
<span data-ttu-id="5a3ef-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-112">This parameter is required.</span></span>

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

### <span data-ttu-id="5a3ef-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="5a3ef-113">-Context</span></span>
<span data-ttu-id="5a3ef-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5a3ef-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-115">This parameter is required.</span></span>

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

### <span data-ttu-id="5a3ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a3ef-116">-DefaultProfile</span></span>
<span data-ttu-id="5a3ef-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a3ef-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a3ef-118">-PassThru</span></span>
<span data-ttu-id="5a3ef-119">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5a3ef-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-120">This parameter is optional.</span></span>
<span data-ttu-id="5a3ef-121">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-121">Default value is false.</span></span>

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

### <span data-ttu-id="5a3ef-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a3ef-122">-Confirm</span></span>
<span data-ttu-id="5a3ef-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a3ef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a3ef-124">-WhatIf</span></span>
<span data-ttu-id="5a3ef-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a3ef-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a3ef-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a3ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a3ef-127">CommonParameters</span></span>
<span data-ttu-id="5a3ef-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a3ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a3ef-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a3ef-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a3ef-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a3ef-130">INPUTS</span></span>

### <span data-ttu-id="5a3ef-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a3ef-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a3ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5a3ef-132">System.String</span></span>

### <span data-ttu-id="5a3ef-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5a3ef-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a3ef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a3ef-134">OUTPUTS</span></span>

### <span data-ttu-id="5a3ef-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a3ef-135">System.Boolean</span></span>

## <span data-ttu-id="5a3ef-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a3ef-136">NOTES</span></span>

## <span data-ttu-id="5a3ef-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a3ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a3ef-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5a3ef-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="5a3ef-139">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5a3ef-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="5a3ef-140">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="5a3ef-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="5a3ef-141">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="5a3ef-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="5a3ef-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="5a3ef-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
