---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 31e2151e5c41a4e4c9d053174f9d598cd16680f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668003"
---
# <span data-ttu-id="83d78-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="83d78-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="83d78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83d78-102">SYNOPSIS</span></span>
<span data-ttu-id="83d78-103">Egy adott API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83d78-103">Removes a particular API Release</span></span>

## <span data-ttu-id="83d78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83d78-104">SYNTAX</span></span>

### <span data-ttu-id="83d78-105">ByApiReleaseId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83d78-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83d78-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83d78-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d78-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83d78-107">DESCRIPTION</span></span>

<span data-ttu-id="83d78-108">A **Remove-AzAzureRmApiManagementApiRelease** parancsmag eltávolítja a meglévő API-kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="83d78-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="83d78-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83d78-109">EXAMPLES</span></span>

### <span data-ttu-id="83d78-110">1. példa: API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="83d78-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="83d78-111">Ez a parancs eltávolítja az API-kiadást a megadott ApiId és ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="83d78-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="83d78-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83d78-112">PARAMETERS</span></span>

### <span data-ttu-id="83d78-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="83d78-113">-ApiId</span></span>
<span data-ttu-id="83d78-114">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="83d78-114">Identifier of the API.</span></span>
<span data-ttu-id="83d78-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="83d78-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d78-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="83d78-116">-Context</span></span>
<span data-ttu-id="83d78-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="83d78-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="83d78-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="83d78-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d78-119">-DefaultProfile</span></span>
<span data-ttu-id="83d78-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83d78-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d78-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83d78-121">-InputObject</span></span>
<span data-ttu-id="83d78-122">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="83d78-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="83d78-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="83d78-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83d78-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83d78-124">-PassThru</span></span>
<span data-ttu-id="83d78-125">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="83d78-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="83d78-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="83d78-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d78-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="83d78-127">-ReleaseId</span></span>
<span data-ttu-id="83d78-128">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83d78-128">Identifier of the API Release.</span></span>
<span data-ttu-id="83d78-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="83d78-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d78-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83d78-130">-Confirm</span></span>
<span data-ttu-id="83d78-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83d78-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d78-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d78-132">-WhatIf</span></span>
<span data-ttu-id="83d78-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83d78-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83d78-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83d78-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d78-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d78-135">CommonParameters</span></span>
<span data-ttu-id="83d78-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83d78-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d78-137">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="83d78-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d78-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83d78-138">INPUTS</span></span>

### <span data-ttu-id="83d78-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83d78-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83d78-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="83d78-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="83d78-141">System. String</span><span class="sxs-lookup"><span data-stu-id="83d78-141">System.String</span></span>

## <span data-ttu-id="83d78-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83d78-142">OUTPUTS</span></span>

### <span data-ttu-id="83d78-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83d78-143">System.Boolean</span></span>

## <span data-ttu-id="83d78-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83d78-144">NOTES</span></span>

## <span data-ttu-id="83d78-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83d78-145">RELATED LINKS</span></span>

[<span data-ttu-id="83d78-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="83d78-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="83d78-147">Új – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="83d78-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="83d78-148">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="83d78-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)