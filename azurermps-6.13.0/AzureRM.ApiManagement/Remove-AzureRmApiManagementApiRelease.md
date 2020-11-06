---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492081"
---
# <span data-ttu-id="aa10d-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa10d-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="aa10d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa10d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa10d-103">Egy adott API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa10d-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa10d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa10d-104">SYNTAX</span></span>

### <span data-ttu-id="aa10d-105">ByApiReleaseId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aa10d-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa10d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa10d-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa10d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa10d-107">DESCRIPTION</span></span>

<span data-ttu-id="aa10d-108">A **Remove-AzureRmApiManagementApiRelease** parancsmag eltávolítja a meglévő API-kiadásokat.</span><span class="sxs-lookup"><span data-stu-id="aa10d-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="aa10d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aa10d-109">EXAMPLES</span></span>

### <span data-ttu-id="aa10d-110">1. példa: API-kiadás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa10d-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="aa10d-111">Ez a parancs eltávolítja az API-kiadást a megadott ApiId és ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="aa10d-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="aa10d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa10d-112">PARAMETERS</span></span>

### <span data-ttu-id="aa10d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa10d-113">-ApiId</span></span>
<span data-ttu-id="aa10d-114">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="aa10d-114">Identifier of the API.</span></span>
<span data-ttu-id="aa10d-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="aa10d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="aa10d-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aa10d-116">-Context</span></span>
<span data-ttu-id="aa10d-117">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="aa10d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aa10d-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="aa10d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="aa10d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa10d-119">-DefaultProfile</span></span>
<span data-ttu-id="aa10d-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa10d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa10d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa10d-121">-InputObject</span></span>
<span data-ttu-id="aa10d-122">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="aa10d-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="aa10d-123">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="aa10d-123">This parameter is required.</span></span>

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

### <span data-ttu-id="aa10d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa10d-124">-PassThru</span></span>
<span data-ttu-id="aa10d-125">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="aa10d-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="aa10d-126">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="aa10d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="aa10d-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="aa10d-127">-ReleaseId</span></span>
<span data-ttu-id="aa10d-128">Az API-kiadás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="aa10d-128">Identifier of the API Release.</span></span>
<span data-ttu-id="aa10d-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="aa10d-129">This parameter is required.</span></span>

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

### <span data-ttu-id="aa10d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa10d-130">-Confirm</span></span>
<span data-ttu-id="aa10d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa10d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa10d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa10d-132">-WhatIf</span></span>
<span data-ttu-id="aa10d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa10d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa10d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa10d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa10d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa10d-135">CommonParameters</span></span>
<span data-ttu-id="aa10d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa10d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa10d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa10d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa10d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa10d-138">INPUTS</span></span>

### <span data-ttu-id="aa10d-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa10d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa10d-140">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa10d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="aa10d-141">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa10d-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aa10d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="aa10d-142">System.String</span></span>

## <span data-ttu-id="aa10d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa10d-143">OUTPUTS</span></span>

### <span data-ttu-id="aa10d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa10d-144">System.Boolean</span></span>

## <span data-ttu-id="aa10d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa10d-145">NOTES</span></span>

## <span data-ttu-id="aa10d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa10d-146">RELATED LINKS</span></span>

[<span data-ttu-id="aa10d-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa10d-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="aa10d-148">Új – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa10d-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="aa10d-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aa10d-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
