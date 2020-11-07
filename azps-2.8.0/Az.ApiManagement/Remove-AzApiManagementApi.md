---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 3aedfc34d3f11abeea598e3ab5a891a3f4ee4526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668006"
---
# <span data-ttu-id="aa187-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="aa187-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa187-102">SYNOPSIS</span></span>
<span data-ttu-id="aa187-103">API eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="aa187-103">Removes an API.</span></span>

## <span data-ttu-id="aa187-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa187-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa187-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa187-105">DESCRIPTION</span></span>
<span data-ttu-id="aa187-106">A **Remove-AzApiManagementApi** parancsmag eltávolítja a meglévő API-t.</span><span class="sxs-lookup"><span data-stu-id="aa187-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="aa187-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa187-107">EXAMPLES</span></span>

### <span data-ttu-id="aa187-108">1. példa: API eltávolítása</span><span class="sxs-lookup"><span data-stu-id="aa187-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="aa187-109">Ez a parancs eltávolítja az API-t a megadott azonosítójú azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="aa187-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="aa187-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa187-110">PARAMETERS</span></span>

### <span data-ttu-id="aa187-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aa187-111">-ApiId</span></span>
<span data-ttu-id="aa187-112">Az API-eltávolítás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa187-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="aa187-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aa187-113">-Context</span></span>
<span data-ttu-id="aa187-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aa187-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aa187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa187-115">-DefaultProfile</span></span>
<span data-ttu-id="aa187-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa187-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa187-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa187-117">-PassThru</span></span>
<span data-ttu-id="aa187-118">passthru</span><span class="sxs-lookup"><span data-stu-id="aa187-118">passthru</span></span>

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

### <span data-ttu-id="aa187-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa187-119">-Confirm</span></span>
<span data-ttu-id="aa187-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa187-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa187-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa187-121">-WhatIf</span></span>
<span data-ttu-id="aa187-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa187-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa187-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa187-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa187-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa187-124">CommonParameters</span></span>
<span data-ttu-id="aa187-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa187-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa187-126">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aa187-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa187-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa187-127">INPUTS</span></span>

### <span data-ttu-id="aa187-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa187-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa187-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aa187-129">System.String</span></span>

### <span data-ttu-id="aa187-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa187-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa187-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa187-131">OUTPUTS</span></span>

### <span data-ttu-id="aa187-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa187-132">System.Boolean</span></span>

## <span data-ttu-id="aa187-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa187-133">NOTES</span></span>

## <span data-ttu-id="aa187-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa187-134">RELATED LINKS</span></span>

[<span data-ttu-id="aa187-135">Exportálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="aa187-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="aa187-137">Importálás – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="aa187-138">Új – AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="aa187-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aa187-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


