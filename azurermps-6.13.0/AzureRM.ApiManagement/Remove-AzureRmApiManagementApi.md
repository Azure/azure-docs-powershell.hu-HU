---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cf27d54e50d320d0ad20a3e847cf2b9dda8ac3c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500300"
---
# <span data-ttu-id="7edb9-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="7edb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7edb9-102">SYNOPSIS</span></span>
<span data-ttu-id="7edb9-103">API eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="7edb9-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7edb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7edb9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7edb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7edb9-105">DESCRIPTION</span></span>
<span data-ttu-id="7edb9-106">A **Remove-AzureRmApiManagementApi** parancsmag eltávolítja a meglévő API-t.</span><span class="sxs-lookup"><span data-stu-id="7edb9-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="7edb9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7edb9-107">EXAMPLES</span></span>

### <span data-ttu-id="7edb9-108">1. példa: API eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7edb9-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="7edb9-109">Ez a parancs eltávolítja az API-t a megadott azonosítójú azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="7edb9-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="7edb9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7edb9-110">PARAMETERS</span></span>

### <span data-ttu-id="7edb9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7edb9-111">-ApiId</span></span>
<span data-ttu-id="7edb9-112">Az API-eltávolítás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7edb9-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="7edb9-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7edb9-113">-Context</span></span>
<span data-ttu-id="7edb9-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7edb9-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7edb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7edb9-115">-DefaultProfile</span></span>
<span data-ttu-id="7edb9-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7edb9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7edb9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7edb9-117">-PassThru</span></span>
<span data-ttu-id="7edb9-118">passthru</span><span class="sxs-lookup"><span data-stu-id="7edb9-118">passthru</span></span>

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

### <span data-ttu-id="7edb9-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7edb9-119">-Confirm</span></span>
<span data-ttu-id="7edb9-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7edb9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7edb9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7edb9-121">-WhatIf</span></span>
<span data-ttu-id="7edb9-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7edb9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7edb9-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7edb9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7edb9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7edb9-124">CommonParameters</span></span>
<span data-ttu-id="7edb9-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7edb9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7edb9-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7edb9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7edb9-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7edb9-127">INPUTS</span></span>

### <span data-ttu-id="7edb9-128">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7edb9-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7edb9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7edb9-129">System.String</span></span>

### <span data-ttu-id="7edb9-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7edb9-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7edb9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7edb9-131">OUTPUTS</span></span>

### <span data-ttu-id="7edb9-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7edb9-132">System.Boolean</span></span>

## <span data-ttu-id="7edb9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7edb9-133">NOTES</span></span>

## <span data-ttu-id="7edb9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7edb9-134">RELATED LINKS</span></span>

[<span data-ttu-id="7edb9-135">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-135">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="7edb9-136">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-136">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="7edb9-137">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-137">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="7edb9-138">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-138">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="7edb9-139">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7edb9-139">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


