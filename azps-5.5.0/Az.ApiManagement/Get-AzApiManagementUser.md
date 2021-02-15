---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143738"
---
# <span data-ttu-id="333cb-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="333cb-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="333cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="333cb-102">SYNOPSIS</span></span>
<span data-ttu-id="333cb-103">Felhasználót vagy felhasználókat kap.</span><span class="sxs-lookup"><span data-stu-id="333cb-103">Gets a user or users.</span></span>

## <span data-ttu-id="333cb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="333cb-104">SYNTAX</span></span>

### <span data-ttu-id="333cb-105">GeAllUsers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="333cb-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="333cb-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="333cb-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="333cb-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="333cb-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="333cb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="333cb-108">DESCRIPTION</span></span>
<span data-ttu-id="333cb-109">A **Get-AzApiManagementUser** parancsmag egy megadott felhasználót vagy az összes felhasználót megkapja, ha nincs megadva felhasználó.</span><span class="sxs-lookup"><span data-stu-id="333cb-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="333cb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="333cb-110">EXAMPLES</span></span>

### <span data-ttu-id="333cb-111">1. példa: Az összes felhasználó lekérte</span><span class="sxs-lookup"><span data-stu-id="333cb-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="333cb-112">Ez a parancs az összes felhasználót beveszi.</span><span class="sxs-lookup"><span data-stu-id="333cb-112">This command gets all users.</span></span>

### <span data-ttu-id="333cb-113">2. példa: Felhasználó lekérte azonosító alapján</span><span class="sxs-lookup"><span data-stu-id="333cb-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="333cb-114">Ez a parancs azonosító alapján kap egy felhasználót.</span><span class="sxs-lookup"><span data-stu-id="333cb-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="333cb-115">3. példa: Felhasználók be szerezni vezetéknév szerint</span><span class="sxs-lookup"><span data-stu-id="333cb-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="333cb-116">Ez a parancs a megadott vezetéknévvel (Fuller) használó felhasználókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="333cb-117">4. példa: Felhasználó lekérte e-mail-cím alapján</span><span class="sxs-lookup"><span data-stu-id="333cb-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="333cb-118">Ez a parancs a megadott e-mail-címmel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="333cb-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="333cb-119">5. példa: Egy csoport összes felhasználója</span><span class="sxs-lookup"><span data-stu-id="333cb-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="333cb-120">Ez a parancs a megadott csoport összes felhasználóját beveszi.</span><span class="sxs-lookup"><span data-stu-id="333cb-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="333cb-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="333cb-121">PARAMETERS</span></span>

### <span data-ttu-id="333cb-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="333cb-122">-Context</span></span>
<span data-ttu-id="333cb-123">A **PsApiManagementContext egy példányát adja meg.**</span><span class="sxs-lookup"><span data-stu-id="333cb-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="333cb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333cb-124">-DefaultProfile</span></span>
<span data-ttu-id="333cb-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="333cb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333cb-126">-Email</span><span class="sxs-lookup"><span data-stu-id="333cb-126">-Email</span></span>
<span data-ttu-id="333cb-127">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="333cb-128">Ha ez a paraméter meg van adva, ez a parancsmag e-mailben talál egy felhasználót.</span><span class="sxs-lookup"><span data-stu-id="333cb-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="333cb-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333cb-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="333cb-130">-FirstName</span></span>
<span data-ttu-id="333cb-131">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="333cb-132">Ha ez a paraméter meg van adva, ez a parancsmag a felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="333cb-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333cb-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="333cb-134">-GroupId</span></span>
<span data-ttu-id="333cb-135">A csoportazonosítót határozza meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-135">Specifies the group identifier.</span></span>
<span data-ttu-id="333cb-136">Ha meg van adva, ez a parancsmag a megadott csoport összes felhasználóját megkeresi.</span><span class="sxs-lookup"><span data-stu-id="333cb-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="333cb-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333cb-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="333cb-138">-LastName</span></span>
<span data-ttu-id="333cb-139">Egy felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="333cb-140">Ha meg van adva, ez a parancsmag vezetéknév szerint megkeresi a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="333cb-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="333cb-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333cb-142">-State</span><span class="sxs-lookup"><span data-stu-id="333cb-142">-State</span></span>
<span data-ttu-id="333cb-143">A felhasználói állapotot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-143">Specifies the user state.</span></span>
<span data-ttu-id="333cb-144">Ha meg van adva, a parancsmag ebben az állapotban találja meg a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="333cb-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="333cb-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333cb-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="333cb-146">-UserId</span></span>
<span data-ttu-id="333cb-147">Felhasználóazonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="333cb-147">Specifies a user ID.</span></span>
<span data-ttu-id="333cb-148">Ha meg van adva, ez a parancsmag megkeresi a felhasználót ezzel az azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="333cb-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="333cb-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="333cb-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="333cb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333cb-150">CommonParameters</span></span>
<span data-ttu-id="333cb-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333cb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333cb-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="333cb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333cb-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="333cb-153">INPUTS</span></span>

### <span data-ttu-id="333cb-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="333cb-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="333cb-155">System.String</span><span class="sxs-lookup"><span data-stu-id="333cb-155">System.String</span></span>

### <span data-ttu-id="333cb-156">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="333cb-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="333cb-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="333cb-157">OUTPUTS</span></span>

### <span data-ttu-id="333cb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="333cb-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="333cb-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="333cb-159">NOTES</span></span>

## <span data-ttu-id="333cb-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="333cb-160">RELATED LINKS</span></span>

[<span data-ttu-id="333cb-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="333cb-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="333cb-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="333cb-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="333cb-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="333cb-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


