---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382253"
---
# <span data-ttu-id="4c82d-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="4c82d-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="4c82d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c82d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c82d-103">Eltávolít egy API-t egy termékből.</span><span class="sxs-lookup"><span data-stu-id="4c82d-103">Removes an API from a product.</span></span>

## <span data-ttu-id="4c82d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4c82d-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c82d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4c82d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c82d-106">A **Remove-AzApiManagementApiFromProduct** parancsmag eltávolítja az Azure API Management API-t egy termékből.</span><span class="sxs-lookup"><span data-stu-id="4c82d-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="4c82d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4c82d-107">EXAMPLES</span></span>

### <span data-ttu-id="4c82d-108">1. példa: API eltávolítása egy termékből</span><span class="sxs-lookup"><span data-stu-id="4c82d-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="4c82d-109">Ez a parancs eltávolítja a megadott API-t egy termékből.</span><span class="sxs-lookup"><span data-stu-id="4c82d-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="4c82d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c82d-110">PARAMETERS</span></span>

### <span data-ttu-id="4c82d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4c82d-111">-ApiId</span></span>
<span data-ttu-id="4c82d-112">A termékből eltávolítható API azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4c82d-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="4c82d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4c82d-113">-Context</span></span>
<span data-ttu-id="4c82d-114">Egy **PsApiManagementContext-et ad meg.**</span><span class="sxs-lookup"><span data-stu-id="4c82d-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4c82d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c82d-115">-DefaultProfile</span></span>
<span data-ttu-id="4c82d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c82d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c82d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c82d-117">-PassThru</span></span>
<span data-ttu-id="4c82d-118">Azt jelzi, hogy ez a parancsmag sikeres $True értéket ad vissza, vagy $False értéket.</span><span class="sxs-lookup"><span data-stu-id="4c82d-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="4c82d-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4c82d-119">-ProductId</span></span>
<span data-ttu-id="4c82d-120">Annak a terméknek az azonosítója, amelyből el szeretné távolítani az API-t.</span><span class="sxs-lookup"><span data-stu-id="4c82d-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="4c82d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c82d-121">CommonParameters</span></span>
<span data-ttu-id="4c82d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c82d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c82d-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c82d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c82d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c82d-124">INPUTS</span></span>

### <span data-ttu-id="4c82d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4c82d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4c82d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4c82d-126">System.String</span></span>

### <span data-ttu-id="4c82d-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c82d-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c82d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c82d-128">OUTPUTS</span></span>

### <span data-ttu-id="4c82d-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c82d-129">System.Boolean</span></span>

## <span data-ttu-id="4c82d-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4c82d-130">NOTES</span></span>

## <span data-ttu-id="4c82d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c82d-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c82d-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="4c82d-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


