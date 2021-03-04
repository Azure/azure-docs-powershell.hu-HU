---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922202"
---
# <span data-ttu-id="3710f-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3710f-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="3710f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3710f-102">SYNOPSIS</span></span>
<span data-ttu-id="3710f-103">Regisztrál egy új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="3710f-103">Registers a new user.</span></span>

## <span data-ttu-id="3710f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3710f-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3710f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3710f-105">DESCRIPTION</span></span>
<span data-ttu-id="3710f-106">A **New-AzApiManagementUser** parancsmag regisztrál egy új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="3710f-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="3710f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3710f-107">EXAMPLES</span></span>

### <span data-ttu-id="3710f-108">1. példa: Új felhasználó regisztrálása</span><span class="sxs-lookup"><span data-stu-id="3710f-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="3710f-109">Ez a parancs regisztrál egy patti Fuller nevű új felhasználót.</span><span class="sxs-lookup"><span data-stu-id="3710f-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="3710f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3710f-110">PARAMETERS</span></span>

### <span data-ttu-id="3710f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3710f-111">-Context</span></span>
<span data-ttu-id="3710f-112">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3710f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3710f-113">-DefaultProfile</span></span>
<span data-ttu-id="3710f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3710f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3710f-115">-Email</span><span class="sxs-lookup"><span data-stu-id="3710f-115">-Email</span></span>
<span data-ttu-id="3710f-116">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="3710f-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="3710f-117">-FirstName</span></span>
<span data-ttu-id="3710f-118">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="3710f-119">A paraméternek 1 és 100 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3710f-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="3710f-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="3710f-120">-LastName</span></span>
<span data-ttu-id="3710f-121">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="3710f-122">A paraméternek 1 és 100 karakter között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3710f-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="3710f-123">-Note</span><span class="sxs-lookup"><span data-stu-id="3710f-123">-Note</span></span>
<span data-ttu-id="3710f-124">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-124">Specifies a note about the user.</span></span>
<span data-ttu-id="3710f-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3710f-125">This parameter is optional.</span></span>
<span data-ttu-id="3710f-126">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="3710f-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="3710f-127">-Password</span><span class="sxs-lookup"><span data-stu-id="3710f-127">-Password</span></span>
<span data-ttu-id="3710f-128">A felhasználói jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-128">Specifies the user password.</span></span>
<span data-ttu-id="3710f-129">Ezt a paramétert kötelező megadni.</span><span class="sxs-lookup"><span data-stu-id="3710f-129">This parameter is required.</span></span>

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

### <span data-ttu-id="3710f-130">-State</span><span class="sxs-lookup"><span data-stu-id="3710f-130">-State</span></span>
<span data-ttu-id="3710f-131">A felhasználói állapotot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-131">Specifies the user state.</span></span>
<span data-ttu-id="3710f-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3710f-132">This parameter is optional.</span></span>
<span data-ttu-id="3710f-133">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="3710f-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="3710f-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="3710f-134">-UserId</span></span>
<span data-ttu-id="3710f-135">A felhasználóazonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="3710f-135">Specifies the user ID.</span></span>
<span data-ttu-id="3710f-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="3710f-136">This parameter is optional.</span></span>
<span data-ttu-id="3710f-137">Ha nincs megadva ez a paraméter, ez a parancsmag létrehoz egy felhasználói azonosítót.</span><span class="sxs-lookup"><span data-stu-id="3710f-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="3710f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3710f-138">CommonParameters</span></span>
<span data-ttu-id="3710f-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3710f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3710f-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3710f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3710f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3710f-141">INPUTS</span></span>

### <span data-ttu-id="3710f-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3710f-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3710f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3710f-143">System.String</span></span>

### <span data-ttu-id="3710f-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="3710f-144">System.Security.SecureString</span></span>

### <span data-ttu-id="3710f-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3710f-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3710f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3710f-146">OUTPUTS</span></span>

### <span data-ttu-id="3710f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3710f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="3710f-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3710f-148">NOTES</span></span>

## <span data-ttu-id="3710f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3710f-149">RELATED LINKS</span></span>

[<span data-ttu-id="3710f-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3710f-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="3710f-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3710f-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


