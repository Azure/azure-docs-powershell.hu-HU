---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495491"
---
# <span data-ttu-id="f0151-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0151-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="f0151-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0151-102">SYNOPSIS</span></span>
<span data-ttu-id="f0151-103">Felhasználót vagy felhasználókat kap.</span><span class="sxs-lookup"><span data-stu-id="f0151-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0151-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0151-104">SYNTAX</span></span>

### <span data-ttu-id="f0151-105">GeAllUsers (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f0151-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0151-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="f0151-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0151-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="f0151-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0151-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0151-108">DESCRIPTION</span></span>
<span data-ttu-id="f0151-109">A **Get-AzureRmApiManagementUser** parancsmag egy megadott felhasználó vagy minden felhasználó számára elérhető, ha nincs megadva felhasználó.</span><span class="sxs-lookup"><span data-stu-id="f0151-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="f0151-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f0151-110">EXAMPLES</span></span>

### <span data-ttu-id="f0151-111">Példa 1: az összes felhasználó beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0151-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="f0151-112">Ez a parancs minden felhasználóhoz bekerül.</span><span class="sxs-lookup"><span data-stu-id="f0151-112">This command gets all users.</span></span>

### <span data-ttu-id="f0151-113">2. példa: felhasználó AZONOSÍTÓjának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0151-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f0151-114">Ez a parancs AZONOSÍTÓval kapja a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="f0151-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="f0151-115">Példa: a felhasználók beolvasása utónév szerint</span><span class="sxs-lookup"><span data-stu-id="f0151-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="f0151-116">Ez a parancs a megadott vezetéknévvel rendelkező felhasználókat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="f0151-117">Példa 4: felhasználó beszerzése e-mail-címre</span><span class="sxs-lookup"><span data-stu-id="f0151-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="f0151-118">Ez a parancs a megadott e-mail-címmel rendelkező felhasználót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="f0151-119">Példa 5: a csoport minden felhasználójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f0151-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="f0151-120">Ez a parancs a megadott csoport minden felhasználóját bekapja.</span><span class="sxs-lookup"><span data-stu-id="f0151-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="f0151-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0151-121">PARAMETERS</span></span>

### <span data-ttu-id="f0151-122">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f0151-122">-Context</span></span>
<span data-ttu-id="f0151-123">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0151-124">-DefaultProfile</span></span>
<span data-ttu-id="f0151-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0151-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-126">– E-mail</span><span class="sxs-lookup"><span data-stu-id="f0151-126">-Email</span></span>
<span data-ttu-id="f0151-127">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="f0151-128">Ha ez a paraméter van megadva, ez a parancsmag a felhasználót e-mailben keresi meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="f0151-129">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-130">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="f0151-130">-FirstName</span></span>
<span data-ttu-id="f0151-131">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="f0151-132">Ha meg van adva ez a paraméter, akkor ez a parancsmag a felhasználó vezetéknevét keresi meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="f0151-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f0151-134">-GroupId</span></span>
<span data-ttu-id="f0151-135">A csoport azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-135">Specifies the group identifier.</span></span>
<span data-ttu-id="f0151-136">Ha meg van adva, ez a parancsmag a megadott csoport összes felhasználóját megkeresi.</span><span class="sxs-lookup"><span data-stu-id="f0151-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="f0151-137">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-138">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="f0151-138">-LastName</span></span>
<span data-ttu-id="f0151-139">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="f0151-140">Ha meg van adva, ez a parancsmag a vezetéknév alapján keresi a felhasználókat.</span><span class="sxs-lookup"><span data-stu-id="f0151-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="f0151-141">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-142">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f0151-142">-State</span></span>
<span data-ttu-id="f0151-143">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-143">Specifies the user state.</span></span>
<span data-ttu-id="f0151-144">Ha meg van adva, ez a parancsmag megkeresi a felhasználókat ebben az államban.</span><span class="sxs-lookup"><span data-stu-id="f0151-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="f0151-145">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="f0151-146">-UserId</span></span>
<span data-ttu-id="f0151-147">Egy felhasználói azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-147">Specifies a user ID.</span></span>
<span data-ttu-id="f0151-148">Ha meg van adva, ez a parancsmag a felhasználót az azonosítóval keresi meg.</span><span class="sxs-lookup"><span data-stu-id="f0151-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="f0151-149">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f0151-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0151-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0151-150">CommonParameters</span></span>
<span data-ttu-id="f0151-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0151-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0151-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0151-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0151-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0151-153">INPUTS</span></span>

### <span data-ttu-id="f0151-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="f0151-154">None</span></span>
<span data-ttu-id="f0151-155">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f0151-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0151-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0151-156">OUTPUTS</span></span>

### <span data-ttu-id="f0151-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0151-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="f0151-158">A felhasználó adatai az API-menedzsment szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f0151-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="f0151-159">IList<Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="f0151-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="f0151-160">A felhasználó listája az API-kezelési szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f0151-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="f0151-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0151-161">NOTES</span></span>

## <span data-ttu-id="f0151-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0151-162">RELATED LINKS</span></span>

[<span data-ttu-id="f0151-163">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0151-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="f0151-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0151-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="f0151-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f0151-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


