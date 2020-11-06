---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492616"
---
# <span data-ttu-id="80aab-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="80aab-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="80aab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80aab-102">SYNOPSIS</span></span>
<span data-ttu-id="80aab-103">Felhasználót vagy felhasználókat kap.</span><span class="sxs-lookup"><span data-stu-id="80aab-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80aab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80aab-104">SYNTAX</span></span>

### <span data-ttu-id="80aab-105">Az összes felhasználó beszerzése (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="80aab-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80aab-106">Felhasználó AZONOSÍTÓjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="80aab-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80aab-107">Felhasználók keresése</span><span class="sxs-lookup"><span data-stu-id="80aab-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80aab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="80aab-108">DESCRIPTION</span></span>
<span data-ttu-id="80aab-109">A **Get-AzureRmApiManagementUser** parancsmag egy megadott felhasználó vagy minden felhasználó számára elérhető, ha nincs megadva felhasználó.</span><span class="sxs-lookup"><span data-stu-id="80aab-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="80aab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="80aab-110">EXAMPLES</span></span>

### <span data-ttu-id="80aab-111">Példa 1: az összes felhasználó beszerzése</span><span class="sxs-lookup"><span data-stu-id="80aab-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="80aab-112">Ez a parancs minden felhasználóhoz bekerül.</span><span class="sxs-lookup"><span data-stu-id="80aab-112">This command gets all users.</span></span>

### <span data-ttu-id="80aab-113">2. példa: felhasználó AZONOSÍTÓjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="80aab-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="80aab-114">Ez a parancs AZONOSÍTÓval kapja a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="80aab-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="80aab-115">Példa: a felhasználók beolvasása utónév szerint</span><span class="sxs-lookup"><span data-stu-id="80aab-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="80aab-116">Ez a parancs a megadott vezetéknévvel rendelkező felhasználókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="80aab-117">Példa 4: felhasználó beszerzése e-mail-címre</span><span class="sxs-lookup"><span data-stu-id="80aab-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="80aab-118">Ez a parancs a megadott e-mail-címmel rendelkező felhasználót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="80aab-119">Példa 5: a csoport minden felhasználójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="80aab-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="80aab-120">Ez a parancs a megadott csoport minden felhasználóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="80aab-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="80aab-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80aab-121">PARAMETERS</span></span>

### <span data-ttu-id="80aab-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="80aab-122">-Context</span></span>
<span data-ttu-id="80aab-123">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="80aab-124">– E-mail</span><span class="sxs-lookup"><span data-stu-id="80aab-124">-Email</span></span>
<span data-ttu-id="80aab-125">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="80aab-126">Ha ez a paraméter van megadva, ez a parancsmag a felhasználót e-mailben keresi meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="80aab-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-128">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="80aab-128">-FirstName</span></span>
<span data-ttu-id="80aab-129">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="80aab-130">Ha meg van adva ez a paraméter, akkor ez a parancsmag a felhasználó vezetéknevét keresi meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="80aab-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="80aab-132">-GroupId</span></span>
<span data-ttu-id="80aab-133">A csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-133">Specifies the group identifier.</span></span>
<span data-ttu-id="80aab-134">Ha meg van adva, ez a parancsmag a megadott csoport összes felhasználóját megkeresi.</span><span class="sxs-lookup"><span data-stu-id="80aab-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="80aab-135">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-136">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="80aab-136">-LastName</span></span>
<span data-ttu-id="80aab-137">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="80aab-138">Ha meg van adva, ez a parancsmag a vezetéknév alapján keresi a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="80aab-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="80aab-139">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-140">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="80aab-140">-State</span></span>
<span data-ttu-id="80aab-141">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-141">Specifies the user state.</span></span>
<span data-ttu-id="80aab-142">Ha meg van adva, ez a parancsmag megkeresi a felhasználókat ebben az államban.</span><span class="sxs-lookup"><span data-stu-id="80aab-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="80aab-143">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="80aab-144">-UserId</span></span>
<span data-ttu-id="80aab-145">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-145">Specifies a user ID.</span></span>
<span data-ttu-id="80aab-146">Ha meg van adva, ez a parancsmag a felhasználót az azonosítóval keresi meg.</span><span class="sxs-lookup"><span data-stu-id="80aab-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="80aab-147">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="80aab-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80aab-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80aab-148">-DefaultProfile</span></span>
<span data-ttu-id="80aab-149">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80aab-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80aab-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80aab-150">CommonParameters</span></span>
<span data-ttu-id="80aab-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80aab-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80aab-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80aab-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80aab-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80aab-153">INPUTS</span></span>

## <span data-ttu-id="80aab-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80aab-154">OUTPUTS</span></span>

### <span data-ttu-id="80aab-155">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="80aab-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="80aab-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80aab-156">NOTES</span></span>

## <span data-ttu-id="80aab-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80aab-157">RELATED LINKS</span></span>

[<span data-ttu-id="80aab-158">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="80aab-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="80aab-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="80aab-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="80aab-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="80aab-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


