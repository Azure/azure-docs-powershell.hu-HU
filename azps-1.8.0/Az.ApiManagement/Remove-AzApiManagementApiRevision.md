---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 903f053da630dbe3fbbd08d247640b23a1f5f331
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836966"
---
# <span data-ttu-id="ad037-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad037-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="ad037-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad037-102">SYNOPSIS</span></span>
<span data-ttu-id="ad037-103">Adott API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ad037-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="ad037-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad037-104">SYNTAX</span></span>

### <span data-ttu-id="ad037-105">ByApiId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad037-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad037-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad037-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad037-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad037-107">DESCRIPTION</span></span>
<span data-ttu-id="ad037-108">A parancsmag **eltávolítása – a AzApiManagementApiRevision** eltávolítja az adott API-t.</span><span class="sxs-lookup"><span data-stu-id="ad037-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="ad037-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ad037-109">EXAMPLES</span></span>

### <span data-ttu-id="ad037-110">Példa 1: API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ad037-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="ad037-111">Ez a parancs eltávolítja az `2` API `echo-api` -t az API-kezelési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="ad037-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="ad037-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad037-112">PARAMETERS</span></span>

### <span data-ttu-id="ad037-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ad037-113">-ApiId</span></span>
<span data-ttu-id="ad037-114">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ad037-114">Identifier of the API.</span></span>
<span data-ttu-id="ad037-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad037-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad037-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad037-116">-ApiRevision</span></span>
<span data-ttu-id="ad037-117">Az API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="ad037-117">Identifier of the API Revision.</span></span> <span data-ttu-id="ad037-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad037-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad037-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ad037-119">-Context</span></span>
<span data-ttu-id="ad037-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="ad037-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad037-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad037-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad037-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad037-122">-DefaultProfile</span></span>
<span data-ttu-id="ad037-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad037-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad037-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad037-124">-InputObject</span></span>
<span data-ttu-id="ad037-125">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="ad037-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="ad037-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="ad037-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad037-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad037-127">-PassThru</span></span>
<span data-ttu-id="ad037-128">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="ad037-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="ad037-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ad037-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad037-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad037-130">-Confirm</span></span>
<span data-ttu-id="ad037-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad037-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad037-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad037-132">-WhatIf</span></span>
<span data-ttu-id="ad037-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad037-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad037-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad037-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad037-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad037-135">CommonParameters</span></span>
<span data-ttu-id="ad037-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad037-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad037-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad037-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad037-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad037-138">INPUTS</span></span>

### <span data-ttu-id="ad037-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad037-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad037-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ad037-140">System.String</span></span>

### <span data-ttu-id="ad037-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ad037-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="ad037-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad037-142">OUTPUTS</span></span>

### <span data-ttu-id="ad037-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ad037-143">System.Boolean</span></span>

## <span data-ttu-id="ad037-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad037-144">NOTES</span></span>

## <span data-ttu-id="ad037-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad037-145">RELATED LINKS</span></span>

[<span data-ttu-id="ad037-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad037-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="ad037-147">Új – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad037-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="ad037-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad037-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)