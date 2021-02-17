---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205766"
---
# <span data-ttu-id="3e4d2-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e4d2-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="3e4d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4d2-103">Az összes vagy adott API-kezelési csoportot beveszi.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="3e4d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3e4d2-104">SYNTAX</span></span>

### <span data-ttu-id="3e4d2-105">GetAllGroups (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e4d2-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e4d2-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e4d2-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e4d2-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e4d2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3e4d2-109">DESCRIPTION</span></span>
<span data-ttu-id="3e4d2-110">A **Get-AzApiManagementGroup** parancsmag az összes vagy adott API-felügyeleti csoportot megkapja.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="3e4d2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3e4d2-111">EXAMPLES</span></span>

### <span data-ttu-id="3e4d2-112">1. példa: Az összes csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="3e4d2-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="3e4d2-113">Ez a parancs az összes csoportot megkapja.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-113">This command gets all groups.</span></span>

### <span data-ttu-id="3e4d2-114">2. példa: Csoport lekérte azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="3e4d2-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="3e4d2-115">Ez a parancs a 0123456789 nevű csoportazonosítót kapja.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="3e4d2-116">3. példa: Csoport lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="3e4d2-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="3e4d2-117">Ez a parancs a Group0002 nevű csoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="3e4d2-118">4. példa: Az összes felhasználói csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="3e4d2-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="3e4d2-119">Ez a parancs a 0123456789 nevű felhasználói azonosítóval minden felhasználói csoportot lekért.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="3e4d2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e4d2-120">PARAMETERS</span></span>

### <span data-ttu-id="3e4d2-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3e4d2-121">-Context</span></span>
<span data-ttu-id="3e4d2-122">A PsApiManagementContext egy példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="3e4d2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4d2-123">-DefaultProfile</span></span>
<span data-ttu-id="3e4d2-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e4d2-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-125">-GroupId</span></span>
<span data-ttu-id="3e4d2-126">A csoportazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-126">Specifies the group ID.</span></span>
<span data-ttu-id="3e4d2-127">Ha meg van adva, a parancsmag megkísérli megtalálni a csoportot az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d2-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3e4d2-128">-Name</span></span>
<span data-ttu-id="3e4d2-129">A felügyeleti csoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-129">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d2-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-130">-ProductId</span></span>
<span data-ttu-id="3e4d2-131">A meglévő termék azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-131">Identifier of existing product.</span></span>
<span data-ttu-id="3e4d2-132">Ha meg van adva, az összes csoportot visszaadja, amelyhez a termék hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="3e4d2-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d2-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="3e4d2-134">-UserId</span></span>
<span data-ttu-id="3e4d2-135">A meglévő termék azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="3e4d2-136">Ha a parancsmag meg van adva, akkor az összes olyan csoportot visszaadja, amelyhez a termék hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e4d2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4d2-137">CommonParameters</span></span>
<span data-ttu-id="3e4d2-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e4d2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4d2-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e4d2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4d2-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e4d2-140">INPUTS</span></span>

### <span data-ttu-id="3e4d2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3e4d2-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3e4d2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3e4d2-142">System.String</span></span>

## <span data-ttu-id="3e4d2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e4d2-143">OUTPUTS</span></span>

### <span data-ttu-id="3e4d2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e4d2-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="3e4d2-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3e4d2-145">NOTES</span></span>

## <span data-ttu-id="3e4d2-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e4d2-146">RELATED LINKS</span></span>

[<span data-ttu-id="3e4d2-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e4d2-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="3e4d2-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e4d2-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="3e4d2-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e4d2-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


