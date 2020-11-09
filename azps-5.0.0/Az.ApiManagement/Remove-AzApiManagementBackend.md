---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementBackend.md
ms.openlocfilehash: 073b32936be1e1614e495ca680a250498742ba66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300893"
---
# <span data-ttu-id="2b26a-101">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b26a-101">Remove-AzApiManagementBackend</span></span>

## <span data-ttu-id="2b26a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b26a-102">SYNOPSIS</span></span>
<span data-ttu-id="2b26a-103">A backend eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2b26a-103">Removes a Backend.</span></span>

## <span data-ttu-id="2b26a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b26a-104">SYNTAX</span></span>

```
Remove-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b26a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b26a-105">DESCRIPTION</span></span>
<span data-ttu-id="2b26a-106">Eltávolítja az azonosító által az API-menedzsment által megadott hátteret.</span><span class="sxs-lookup"><span data-stu-id="2b26a-106">Removes a backend specified by the Identifier from the Api Management.</span></span>

## <span data-ttu-id="2b26a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2b26a-107">EXAMPLES</span></span>

### <span data-ttu-id="2b26a-108">1. példa: a backend 123 eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2b26a-108">Example 1: Remove the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementBackend -Context $apimContext -BackendId 123 -PassThru
```

## <span data-ttu-id="2b26a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b26a-109">PARAMETERS</span></span>

### <span data-ttu-id="2b26a-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2b26a-110">-BackendId</span></span>
<span data-ttu-id="2b26a-111">A meglévő backend-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2b26a-111">Identifier of existing backend.</span></span>
<span data-ttu-id="2b26a-112">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2b26a-112">This parameter is required.</span></span>

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

### <span data-ttu-id="2b26a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2b26a-113">-Context</span></span>
<span data-ttu-id="2b26a-114">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="2b26a-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b26a-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="2b26a-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b26a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b26a-116">-DefaultProfile</span></span>
<span data-ttu-id="2b26a-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b26a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b26a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b26a-118">-PassThru</span></span>
<span data-ttu-id="2b26a-119">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="2b26a-119">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2b26a-120">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="2b26a-120">This parameter is optional.</span></span>
<span data-ttu-id="2b26a-121">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="2b26a-121">Default value is false.</span></span>

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

### <span data-ttu-id="2b26a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2b26a-122">-Confirm</span></span>
<span data-ttu-id="2b26a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2b26a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b26a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b26a-124">-WhatIf</span></span>
<span data-ttu-id="2b26a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2b26a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b26a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2b26a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b26a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b26a-127">CommonParameters</span></span>
<span data-ttu-id="2b26a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b26a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b26a-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2b26a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b26a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b26a-130">INPUTS</span></span>

### <span data-ttu-id="2b26a-131">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b26a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b26a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b26a-132">System.String</span></span>

### <span data-ttu-id="2b26a-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b26a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b26a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b26a-134">OUTPUTS</span></span>

### <span data-ttu-id="2b26a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2b26a-135">System.Boolean</span></span>

## <span data-ttu-id="2b26a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b26a-136">NOTES</span></span>

## <span data-ttu-id="2b26a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b26a-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b26a-138">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b26a-138">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="2b26a-139">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b26a-139">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="2b26a-140">Új – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2b26a-140">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="2b26a-141">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2b26a-141">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="2b26a-142">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2b26a-142">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)
