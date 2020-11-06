---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492079"
---
# <span data-ttu-id="6d5d1-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6d5d1-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="6d5d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="6d5d1-103">Adott API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6d5d1-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d5d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d5d1-104">SYNTAX</span></span>

### <span data-ttu-id="6d5d1-105">ByApiId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d5d1-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d5d1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d5d1-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d5d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d5d1-107">DESCRIPTION</span></span>
<span data-ttu-id="6d5d1-108">A parancsmag **eltávolítása – a AzureRmApiManagementApiRevision** eltávolítja az adott API-t.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="6d5d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6d5d1-109">EXAMPLES</span></span>

### <span data-ttu-id="6d5d1-110">Példa 1: API-módosítás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6d5d1-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="6d5d1-111">Ez a parancs eltávolítja az `2` API `echo-api` -t az API-kezelési szolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="6d5d1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d5d1-112">PARAMETERS</span></span>

### <span data-ttu-id="6d5d1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6d5d1-113">-ApiId</span></span>
<span data-ttu-id="6d5d1-114">Az API-azonosító.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-114">Identifier of the API.</span></span>
<span data-ttu-id="6d5d1-115">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6d5d1-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6d5d1-116">-ApiRevision</span></span>
<span data-ttu-id="6d5d1-117">Az API-verzió verziószámának azonosítója</span><span class="sxs-lookup"><span data-stu-id="6d5d1-117">Identifier of the API Revision.</span></span> <span data-ttu-id="6d5d1-118">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6d5d1-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6d5d1-119">-Context</span></span>
<span data-ttu-id="6d5d1-120">A PsApiManagementContext példánya.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6d5d1-121">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6d5d1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d5d1-122">-DefaultProfile</span></span>
<span data-ttu-id="6d5d1-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d5d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d5d1-124">-InputObject</span></span>
<span data-ttu-id="6d5d1-125">A PsApiManagementApiRelease példánya.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="6d5d1-126">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-126">This parameter is required.</span></span>

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

### <span data-ttu-id="6d5d1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d5d1-127">-PassThru</span></span>
<span data-ttu-id="6d5d1-128">Ha a megadott művelet sikeres, akkor a True Write True értékre vált.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6d5d1-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d5d1-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d5d1-130">-Confirm</span></span>
<span data-ttu-id="6d5d1-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d5d1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d5d1-132">-WhatIf</span></span>
<span data-ttu-id="6d5d1-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d5d1-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d5d1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d5d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d5d1-135">CommonParameters</span></span>
<span data-ttu-id="6d5d1-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d5d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d5d1-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d5d1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d5d1-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d5d1-138">INPUTS</span></span>

### <span data-ttu-id="6d5d1-139">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6d5d1-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d5d1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6d5d1-140">System.String</span></span>

### <span data-ttu-id="6d5d1-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6d5d1-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="6d5d1-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d5d1-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6d5d1-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d5d1-143">OUTPUTS</span></span>

### <span data-ttu-id="6d5d1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d5d1-144">System.Boolean</span></span>

## <span data-ttu-id="6d5d1-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d5d1-145">NOTES</span></span>

## <span data-ttu-id="6d5d1-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d5d1-146">RELATED LINKS</span></span>

[<span data-ttu-id="6d5d1-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6d5d1-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="6d5d1-148">Új – AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6d5d1-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="6d5d1-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6d5d1-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
