---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332357"
---
# <span data-ttu-id="e46f5-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="e46f5-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="e46f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e46f5-103">Hozzáad egy terméket egy csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e46f5-103">Adds a product to a group.</span></span>

## <span data-ttu-id="e46f5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e46f5-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e46f5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e46f5-105">DESCRIPTION</span></span>
<span data-ttu-id="e46f5-106">Az **Add-AzApiManagementProductToGroup** parancsmag hozzáad egy terméket egy meglévő csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e46f5-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="e46f5-107">Más szóval ez a parancsmag hozzárendel egy csoportot egy termékhez.</span><span class="sxs-lookup"><span data-stu-id="e46f5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="e46f5-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e46f5-108">EXAMPLES</span></span>

### <span data-ttu-id="e46f5-109">1. példa: Termék hozzáadása csoporthoz</span><span class="sxs-lookup"><span data-stu-id="e46f5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="e46f5-110">Ez a parancs hozzáad egy terméket egy meglévő csoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e46f5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="e46f5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e46f5-111">PARAMETERS</span></span>

### <span data-ttu-id="e46f5-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e46f5-112">-Context</span></span>
<span data-ttu-id="e46f5-113">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="e46f5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e46f5-114">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e46f5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="e46f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46f5-115">-DefaultProfile</span></span>
<span data-ttu-id="e46f5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e46f5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e46f5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e46f5-117">-GroupId</span></span>
<span data-ttu-id="e46f5-118">A csoportazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46f5-118">Specifies the group ID.</span></span>
<span data-ttu-id="e46f5-119">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e46f5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="e46f5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e46f5-120">-PassThru</span></span>
<span data-ttu-id="e46f5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="e46f5-121">passthru</span></span>

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

### <span data-ttu-id="e46f5-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e46f5-122">-ProductId</span></span>
<span data-ttu-id="e46f5-123">A termékazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e46f5-123">Specifies the product ID.</span></span>
<span data-ttu-id="e46f5-124">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="e46f5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="e46f5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46f5-125">CommonParameters</span></span>
<span data-ttu-id="e46f5-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e46f5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46f5-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e46f5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46f5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e46f5-128">INPUTS</span></span>

### <span data-ttu-id="e46f5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e46f5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e46f5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e46f5-130">System.String</span></span>

### <span data-ttu-id="e46f5-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e46f5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e46f5-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e46f5-132">OUTPUTS</span></span>

### <span data-ttu-id="e46f5-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e46f5-133">System.Boolean</span></span>

## <span data-ttu-id="e46f5-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e46f5-134">NOTES</span></span>

## <span data-ttu-id="e46f5-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e46f5-135">RELATED LINKS</span></span>

[<span data-ttu-id="e46f5-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="e46f5-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


