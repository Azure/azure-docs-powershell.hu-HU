---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018011"
---
# <span data-ttu-id="fb70e-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="fb70e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb70e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb70e-103">Felhasználót vagy felhasználókat kap.</span><span class="sxs-lookup"><span data-stu-id="fb70e-103">Gets a user or users.</span></span>

## <span data-ttu-id="fb70e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb70e-104">SYNTAX</span></span>

### <span data-ttu-id="fb70e-105">GeAllUsers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb70e-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb70e-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="fb70e-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb70e-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb70e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb70e-108">DESCRIPTION</span></span>
<span data-ttu-id="fb70e-109">A **Get-AzApiManagementUser** parancsmag egy megadott felhasználó vagy minden felhasználó számára elérhető, ha nincs megadva felhasználó.</span><span class="sxs-lookup"><span data-stu-id="fb70e-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="fb70e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fb70e-110">EXAMPLES</span></span>

### <span data-ttu-id="fb70e-111">Példa 1: az összes felhasználó beszerzése</span><span class="sxs-lookup"><span data-stu-id="fb70e-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="fb70e-112">Ez a parancs minden felhasználóhoz bekerül.</span><span class="sxs-lookup"><span data-stu-id="fb70e-112">This command gets all users.</span></span>

### <span data-ttu-id="fb70e-113">2. példa: felhasználó AZONOSÍTÓjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fb70e-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="fb70e-114">Ez a parancs AZONOSÍTÓval kapja a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="fb70e-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="fb70e-115">3. példa: a felhasználók beszerzése utónév szerint</span><span class="sxs-lookup"><span data-stu-id="fb70e-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="fb70e-116">Ez a parancs a megadott vezetéknévvel rendelkező felhasználókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="fb70e-117">Példa 4: felhasználó beszerzése e-mail-címre</span><span class="sxs-lookup"><span data-stu-id="fb70e-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="fb70e-118">Ez a parancs a megadott e-mail-címmel rendelkező felhasználót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="fb70e-119">Példa 5: a csoport minden felhasználójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="fb70e-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="fb70e-120">Ez a parancs a megadott csoport minden felhasználóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="fb70e-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="fb70e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb70e-121">PARAMETERS</span></span>

### <span data-ttu-id="fb70e-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fb70e-122">-Context</span></span>
<span data-ttu-id="fb70e-123">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="fb70e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb70e-124">-DefaultProfile</span></span>
<span data-ttu-id="fb70e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb70e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb70e-126">– E-mail</span><span class="sxs-lookup"><span data-stu-id="fb70e-126">-Email</span></span>
<span data-ttu-id="fb70e-127">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="fb70e-128">Ha ez a paraméter van megadva, ez a parancsmag a felhasználót e-mailben keresi meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="fb70e-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-130">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="fb70e-130">-FirstName</span></span>
<span data-ttu-id="fb70e-131">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="fb70e-132">Ha meg van adva ez a paraméter, akkor ez a parancsmag a felhasználó vezetéknevét keresi meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="fb70e-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fb70e-134">-GroupId</span></span>
<span data-ttu-id="fb70e-135">A csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-135">Specifies the group identifier.</span></span>
<span data-ttu-id="fb70e-136">Ha meg van adva, ez a parancsmag a megadott csoport összes felhasználóját megkeresi.</span><span class="sxs-lookup"><span data-stu-id="fb70e-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="fb70e-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-138">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="fb70e-138">-LastName</span></span>
<span data-ttu-id="fb70e-139">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="fb70e-140">Ha meg van adva, ez a parancsmag a vezetéknév alapján keresi a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="fb70e-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="fb70e-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-142">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="fb70e-142">-State</span></span>
<span data-ttu-id="fb70e-143">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-143">Specifies the user state.</span></span>
<span data-ttu-id="fb70e-144">Ha meg van adva, ez a parancsmag megkeresi a felhasználókat ebben az államban.</span><span class="sxs-lookup"><span data-stu-id="fb70e-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="fb70e-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="fb70e-146">-UserId</span></span>
<span data-ttu-id="fb70e-147">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-147">Specifies a user ID.</span></span>
<span data-ttu-id="fb70e-148">Ha meg van adva, ez a parancsmag a felhasználót az azonosítóval keresi meg.</span><span class="sxs-lookup"><span data-stu-id="fb70e-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="fb70e-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="fb70e-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb70e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb70e-150">CommonParameters</span></span>
<span data-ttu-id="fb70e-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb70e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb70e-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb70e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb70e-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb70e-153">INPUTS</span></span>

### <span data-ttu-id="fb70e-154">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fb70e-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb70e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="fb70e-155">System.String</span></span>

### <span data-ttu-id="fb70e-156">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementUserState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fb70e-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fb70e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb70e-157">OUTPUTS</span></span>

### <span data-ttu-id="fb70e-158">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="fb70e-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb70e-159">NOTES</span></span>

## <span data-ttu-id="fb70e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb70e-160">RELATED LINKS</span></span>

[<span data-ttu-id="fb70e-161">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="fb70e-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="fb70e-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fb70e-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


