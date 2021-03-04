---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 05f3ac10171c9135b59b9fb6894f5b5fbf670de0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923065"
---
# <span data-ttu-id="f9733-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f9733-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="f9733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9733-102">SYNOPSIS</span></span>
<span data-ttu-id="f9733-103">Eltávolít egy terméket egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="f9733-103">Removes a product from a group.</span></span>

## <span data-ttu-id="f9733-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9733-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9733-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9733-105">DESCRIPTION</span></span>
<span data-ttu-id="f9733-106">A **Remove-AzApiManagementProductFromGroup** parancsmag eltávolít egy terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="f9733-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="f9733-107">Más szóval ez a parancsmag eltávolítja a csoport-hozzárendelést egy termékből.</span><span class="sxs-lookup"><span data-stu-id="f9733-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="f9733-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9733-108">EXAMPLES</span></span>

### <span data-ttu-id="f9733-109">1. példa: Termék eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="f9733-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f9733-110">Ez a parancs eltávolít egy terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="f9733-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="f9733-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9733-111">PARAMETERS</span></span>

### <span data-ttu-id="f9733-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f9733-112">-Context</span></span>
<span data-ttu-id="f9733-113">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="f9733-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f9733-114">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f9733-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f9733-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9733-115">-DefaultProfile</span></span>
<span data-ttu-id="f9733-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9733-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9733-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f9733-117">-GroupId</span></span>
<span data-ttu-id="f9733-118">A csoportazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9733-118">Specifies the group ID.</span></span>
<span data-ttu-id="f9733-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f9733-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f9733-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9733-120">-PassThru</span></span>
<span data-ttu-id="f9733-121">Azt jelzi, hogy ez a parancsmag sikeres $True értéket ad eredményül, illetve $False értéket.</span><span class="sxs-lookup"><span data-stu-id="f9733-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f9733-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f9733-122">-ProductId</span></span>
<span data-ttu-id="f9733-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9733-123">Specifies the product ID.</span></span>
<span data-ttu-id="f9733-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="f9733-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f9733-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9733-125">CommonParameters</span></span>
<span data-ttu-id="f9733-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9733-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9733-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9733-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9733-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9733-128">INPUTS</span></span>

### <span data-ttu-id="f9733-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f9733-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f9733-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f9733-130">System.String</span></span>

### <span data-ttu-id="f9733-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9733-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9733-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9733-132">OUTPUTS</span></span>

### <span data-ttu-id="f9733-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9733-133">System.Boolean</span></span>

## <span data-ttu-id="f9733-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9733-134">NOTES</span></span>

## <span data-ttu-id="f9733-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9733-135">RELATED LINKS</span></span>

[<span data-ttu-id="f9733-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f9733-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


