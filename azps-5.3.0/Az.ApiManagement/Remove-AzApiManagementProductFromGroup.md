---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381918"
---
# <span data-ttu-id="547d9-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="547d9-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="547d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="547d9-102">SYNOPSIS</span></span>
<span data-ttu-id="547d9-103">Eltávolít egy terméket egy csoportból.</span><span class="sxs-lookup"><span data-stu-id="547d9-103">Removes a product from a group.</span></span>

## <span data-ttu-id="547d9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="547d9-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547d9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="547d9-105">DESCRIPTION</span></span>
<span data-ttu-id="547d9-106">A **Remove-AzApiManagementProductFromGroup** parancsmag eltávolít egy terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="547d9-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="547d9-107">Más szóval ez a parancsmag eltávolítja a csoport-hozzárendelést egy termékből.</span><span class="sxs-lookup"><span data-stu-id="547d9-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="547d9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="547d9-108">EXAMPLES</span></span>

### <span data-ttu-id="547d9-109">1. példa: Termék eltávolítása egy csoportból</span><span class="sxs-lookup"><span data-stu-id="547d9-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="547d9-110">Ez a parancs eltávolít egy terméket egy meglévő csoportból.</span><span class="sxs-lookup"><span data-stu-id="547d9-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="547d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="547d9-111">PARAMETERS</span></span>

### <span data-ttu-id="547d9-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="547d9-112">-Context</span></span>
<span data-ttu-id="547d9-113">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="547d9-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="547d9-114">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="547d9-114">This parameter is required.</span></span>

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

### <span data-ttu-id="547d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547d9-115">-DefaultProfile</span></span>
<span data-ttu-id="547d9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="547d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="547d9-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="547d9-117">-GroupId</span></span>
<span data-ttu-id="547d9-118">A csoportazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="547d9-118">Specifies the group ID.</span></span>
<span data-ttu-id="547d9-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="547d9-119">This parameter is required.</span></span>

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

### <span data-ttu-id="547d9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="547d9-120">-PassThru</span></span>
<span data-ttu-id="547d9-121">Azt jelzi, hogy ez a parancsmag sikeres $True értéket ad eredményül, illetve $False értéket.</span><span class="sxs-lookup"><span data-stu-id="547d9-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="547d9-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="547d9-122">-ProductId</span></span>
<span data-ttu-id="547d9-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="547d9-123">Specifies the product ID.</span></span>
<span data-ttu-id="547d9-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="547d9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="547d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547d9-125">CommonParameters</span></span>
<span data-ttu-id="547d9-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="547d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547d9-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="547d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547d9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="547d9-128">INPUTS</span></span>

### <span data-ttu-id="547d9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="547d9-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="547d9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="547d9-130">System.String</span></span>

### <span data-ttu-id="547d9-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="547d9-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="547d9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="547d9-132">OUTPUTS</span></span>

### <span data-ttu-id="547d9-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="547d9-133">System.Boolean</span></span>

## <span data-ttu-id="547d9-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="547d9-134">NOTES</span></span>

## <span data-ttu-id="547d9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="547d9-135">RELATED LINKS</span></span>

[<span data-ttu-id="547d9-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="547d9-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


