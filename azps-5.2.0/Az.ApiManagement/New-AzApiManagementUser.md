---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366126"
---
# <span data-ttu-id="354bc-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="354bc-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="354bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354bc-102">SYNOPSIS</span></span>
<span data-ttu-id="354bc-103">Regisztrál egy új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="354bc-103">Registers a new user.</span></span>

## <span data-ttu-id="354bc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="354bc-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354bc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="354bc-105">DESCRIPTION</span></span>
<span data-ttu-id="354bc-106">A **New-AzApiManagementUser** parancsmag regisztrál egy új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="354bc-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="354bc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="354bc-107">EXAMPLES</span></span>

### <span data-ttu-id="354bc-108">1. példa: Új felhasználó regisztrálása</span><span class="sxs-lookup"><span data-stu-id="354bc-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="354bc-109">Ez a parancs regisztrál egy patti Fuller nevű új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="354bc-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="354bc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354bc-110">PARAMETERS</span></span>

### <span data-ttu-id="354bc-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="354bc-111">-Context</span></span>
<span data-ttu-id="354bc-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="354bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354bc-113">-DefaultProfile</span></span>
<span data-ttu-id="354bc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="354bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="354bc-115">-Email</span><span class="sxs-lookup"><span data-stu-id="354bc-115">-Email</span></span>
<span data-ttu-id="354bc-116">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="354bc-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="354bc-117">-FirstName</span></span>
<span data-ttu-id="354bc-118">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="354bc-119">A paraméternek 1 és 100 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="354bc-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="354bc-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="354bc-120">-LastName</span></span>
<span data-ttu-id="354bc-121">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="354bc-122">A paraméternek 1 és 100 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="354bc-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="354bc-123">-Note</span><span class="sxs-lookup"><span data-stu-id="354bc-123">-Note</span></span>
<span data-ttu-id="354bc-124">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-124">Specifies a note about the user.</span></span>
<span data-ttu-id="354bc-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="354bc-125">This parameter is optional.</span></span>
<span data-ttu-id="354bc-126">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="354bc-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="354bc-127">-Password</span><span class="sxs-lookup"><span data-stu-id="354bc-127">-Password</span></span>
<span data-ttu-id="354bc-128">A felhasználói jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-128">Specifies the user password.</span></span>
<span data-ttu-id="354bc-129">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="354bc-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354bc-130">-State</span><span class="sxs-lookup"><span data-stu-id="354bc-130">-State</span></span>
<span data-ttu-id="354bc-131">A felhasználói állapotot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-131">Specifies the user state.</span></span>
<span data-ttu-id="354bc-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="354bc-132">This parameter is optional.</span></span>
<span data-ttu-id="354bc-133">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="354bc-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354bc-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="354bc-134">-UserId</span></span>
<span data-ttu-id="354bc-135">A felhasználóazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="354bc-135">Specifies the user ID.</span></span>
<span data-ttu-id="354bc-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="354bc-136">This parameter is optional.</span></span>
<span data-ttu-id="354bc-137">Ha nincs megadva ez a paraméter, ez a parancsmag létrehoz egy felhasználói azonosítót.</span><span class="sxs-lookup"><span data-stu-id="354bc-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="354bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354bc-138">CommonParameters</span></span>
<span data-ttu-id="354bc-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354bc-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="354bc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354bc-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="354bc-141">INPUTS</span></span>

### <span data-ttu-id="354bc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="354bc-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="354bc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="354bc-143">System.String</span></span>

### <span data-ttu-id="354bc-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="354bc-144">System.Security.SecureString</span></span>

### <span data-ttu-id="354bc-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="354bc-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="354bc-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="354bc-146">OUTPUTS</span></span>

### <span data-ttu-id="354bc-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="354bc-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="354bc-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="354bc-148">NOTES</span></span>

## <span data-ttu-id="354bc-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="354bc-149">RELATED LINKS</span></span>

[<span data-ttu-id="354bc-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="354bc-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="354bc-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="354bc-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


