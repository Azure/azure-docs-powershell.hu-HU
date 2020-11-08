---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186465"
---
# <span data-ttu-id="12880-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="12880-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="12880-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12880-102">SYNOPSIS</span></span>
<span data-ttu-id="12880-103">Felhasználót vagy felhasználókat kap.</span><span class="sxs-lookup"><span data-stu-id="12880-103">Gets a user or users.</span></span>

## <span data-ttu-id="12880-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12880-104">SYNTAX</span></span>

### <span data-ttu-id="12880-105">GeAllUsers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12880-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12880-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="12880-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12880-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="12880-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12880-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="12880-108">DESCRIPTION</span></span>
<span data-ttu-id="12880-109">A **Get-AzApiManagementUser** parancsmag egy megadott felhasználó vagy minden felhasználó számára elérhető, ha nincs megadva felhasználó.</span><span class="sxs-lookup"><span data-stu-id="12880-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="12880-110">Példák</span><span class="sxs-lookup"><span data-stu-id="12880-110">EXAMPLES</span></span>

### <span data-ttu-id="12880-111">Példa 1: az összes felhasználó beszerzése</span><span class="sxs-lookup"><span data-stu-id="12880-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="12880-112">Ez a parancs minden felhasználóhoz bekerül.</span><span class="sxs-lookup"><span data-stu-id="12880-112">This command gets all users.</span></span>

### <span data-ttu-id="12880-113">2. példa: felhasználó AZONOSÍTÓjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="12880-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="12880-114">Ez a parancs AZONOSÍTÓval kapja a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="12880-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="12880-115">3. példa: a felhasználók beszerzése utónév szerint</span><span class="sxs-lookup"><span data-stu-id="12880-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="12880-116">Ez a parancs a megadott vezetéknévvel rendelkező felhasználókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="12880-117">Példa 4: felhasználó beszerzése e-mail-címre</span><span class="sxs-lookup"><span data-stu-id="12880-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="12880-118">Ez a parancs a megadott e-mail-címmel rendelkező felhasználót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="12880-119">Példa 5: a csoport minden felhasználójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="12880-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="12880-120">Ez a parancs a megadott csoport minden felhasználóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="12880-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="12880-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12880-121">PARAMETERS</span></span>

### <span data-ttu-id="12880-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="12880-122">-Context</span></span>
<span data-ttu-id="12880-123">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="12880-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12880-124">-DefaultProfile</span></span>
<span data-ttu-id="12880-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12880-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12880-126">– E-mail</span><span class="sxs-lookup"><span data-stu-id="12880-126">-Email</span></span>
<span data-ttu-id="12880-127">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="12880-128">Ha ez a paraméter van megadva, ez a parancsmag a felhasználót e-mailben keresi meg.</span><span class="sxs-lookup"><span data-stu-id="12880-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="12880-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-130">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="12880-130">-FirstName</span></span>
<span data-ttu-id="12880-131">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="12880-132">Ha meg van adva ez a paraméter, akkor ez a parancsmag a felhasználó vezetéknevét keresi meg.</span><span class="sxs-lookup"><span data-stu-id="12880-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="12880-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="12880-134">-GroupId</span></span>
<span data-ttu-id="12880-135">A csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-135">Specifies the group identifier.</span></span>
<span data-ttu-id="12880-136">Ha meg van adva, ez a parancsmag a megadott csoport összes felhasználóját megkeresi.</span><span class="sxs-lookup"><span data-stu-id="12880-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="12880-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-138">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="12880-138">-LastName</span></span>
<span data-ttu-id="12880-139">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="12880-140">Ha meg van adva, ez a parancsmag a vezetéknév alapján keresi a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="12880-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="12880-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-142">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="12880-142">-State</span></span>
<span data-ttu-id="12880-143">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="12880-143">Specifies the user state.</span></span>
<span data-ttu-id="12880-144">Ha meg van adva, ez a parancsmag megkeresi a felhasználókat ebben az államban.</span><span class="sxs-lookup"><span data-stu-id="12880-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="12880-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="12880-146">-UserId</span></span>
<span data-ttu-id="12880-147">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="12880-147">Specifies a user ID.</span></span>
<span data-ttu-id="12880-148">Ha meg van adva, ez a parancsmag a felhasználót az azonosítóval keresi meg.</span><span class="sxs-lookup"><span data-stu-id="12880-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="12880-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="12880-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="12880-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12880-150">CommonParameters</span></span>
<span data-ttu-id="12880-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12880-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12880-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="12880-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12880-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12880-153">INPUTS</span></span>

### <span data-ttu-id="12880-154">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12880-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12880-155">System. String</span><span class="sxs-lookup"><span data-stu-id="12880-155">System.String</span></span>

### <span data-ttu-id="12880-156">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementUserState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="12880-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="12880-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12880-157">OUTPUTS</span></span>

### <span data-ttu-id="12880-158">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="12880-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="12880-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12880-159">NOTES</span></span>

## <span data-ttu-id="12880-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12880-160">RELATED LINKS</span></span>

[<span data-ttu-id="12880-161">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="12880-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="12880-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="12880-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="12880-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="12880-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


