---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: fadd9732afe695d5c69f8a5c4838c68461f683d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187671"
---
# <span data-ttu-id="88692-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="88692-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="88692-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88692-102">SYNOPSIS</span></span>
<span data-ttu-id="88692-103">Adott API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="88692-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="88692-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88692-104">SYNTAX</span></span>

### <span data-ttu-id="88692-105">ByApiId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88692-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88692-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="88692-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88692-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88692-107">DESCRIPTION</span></span>
<span data-ttu-id="88692-108">A parancsmag **eltávolítása – a AzApiManagementApiRevision** eltávolítja az adott API-t.</span><span class="sxs-lookup"><span data-stu-id="88692-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="88692-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88692-109">EXAMPLES</span></span>

### <span data-ttu-id="88692-110">Példa 1: API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="88692-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="88692-111">Ez a parancs eltávolítja az `2` API `echo-api` -t az API-kezelési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="88692-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

### <span data-ttu-id="88692-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="88692-112">Example 2</span></span>

<span data-ttu-id="88692-113">Ez a parancs eltávolítja az API echo-API API-kezelési szolgáltatásból való 2 módosítását.</span><span class="sxs-lookup"><span data-stu-id="88692-113">This command removes the 2 revision of the API echo-api from API Management service.</span></span> <span data-ttu-id="88692-114">autogenerated</span><span class="sxs-lookup"><span data-stu-id="88692-114">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzApiManagementApiRevision -ApiId '0001' -ApiRevision 6 -Context <PsApiManagementContext>
```

## <span data-ttu-id="88692-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88692-115">PARAMETERS</span></span>

### <span data-ttu-id="88692-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="88692-116">-ApiId</span></span>
<span data-ttu-id="88692-117">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="88692-117">Identifier of the API.</span></span>
<span data-ttu-id="88692-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="88692-118">This parameter is required.</span></span>

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

### <span data-ttu-id="88692-119">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="88692-119">-ApiRevision</span></span>
<span data-ttu-id="88692-120">Az API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="88692-120">Identifier of the API Revision.</span></span> <span data-ttu-id="88692-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="88692-121">This parameter is required.</span></span>

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

### <span data-ttu-id="88692-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="88692-122">-Context</span></span>
<span data-ttu-id="88692-123">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="88692-123">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="88692-124">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="88692-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88692-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88692-125">-DefaultProfile</span></span>
<span data-ttu-id="88692-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88692-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88692-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88692-127">-InputObject</span></span>
<span data-ttu-id="88692-128">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="88692-128">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="88692-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="88692-129">This parameter is required.</span></span>

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

### <span data-ttu-id="88692-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88692-130">-PassThru</span></span>
<span data-ttu-id="88692-131">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="88692-131">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="88692-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="88692-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="88692-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88692-133">-Confirm</span></span>
<span data-ttu-id="88692-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88692-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88692-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88692-135">-WhatIf</span></span>
<span data-ttu-id="88692-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88692-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88692-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88692-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88692-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88692-138">CommonParameters</span></span>
<span data-ttu-id="88692-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88692-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88692-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="88692-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88692-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88692-141">INPUTS</span></span>

### <span data-ttu-id="88692-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="88692-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="88692-143">System. String</span><span class="sxs-lookup"><span data-stu-id="88692-143">System.String</span></span>

### <span data-ttu-id="88692-144">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="88692-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="88692-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88692-145">OUTPUTS</span></span>

### <span data-ttu-id="88692-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88692-146">System.Boolean</span></span>

## <span data-ttu-id="88692-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88692-147">NOTES</span></span>

## <span data-ttu-id="88692-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88692-148">RELATED LINKS</span></span>

[<span data-ttu-id="88692-149">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="88692-149">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="88692-150">Új – AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="88692-150">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="88692-151">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="88692-151">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)