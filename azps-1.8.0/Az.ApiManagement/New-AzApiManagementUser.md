---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 30ff5f7d9ead2226c6c03b4707af9c20ff40d405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836979"
---
# <span data-ttu-id="1df2f-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1df2f-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="1df2f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1df2f-102">SYNOPSIS</span></span>
<span data-ttu-id="1df2f-103">Új felhasználó regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="1df2f-103">Registers a new user.</span></span>

## <span data-ttu-id="1df2f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1df2f-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1df2f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1df2f-105">DESCRIPTION</span></span>
<span data-ttu-id="1df2f-106">A **New-AzApiManagementUser** parancsmag új felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="1df2f-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="1df2f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1df2f-107">EXAMPLES</span></span>

### <span data-ttu-id="1df2f-108">1. példa: új felhasználó regisztrálása</span><span class="sxs-lookup"><span data-stu-id="1df2f-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="1df2f-109">Ez a parancs egy új, Patti Fuller nevű felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="1df2f-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="1df2f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1df2f-110">PARAMETERS</span></span>

### <span data-ttu-id="1df2f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1df2f-111">-Context</span></span>
<span data-ttu-id="1df2f-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1df2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1df2f-113">-DefaultProfile</span></span>
<span data-ttu-id="1df2f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1df2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1df2f-115">– E-mail</span><span class="sxs-lookup"><span data-stu-id="1df2f-115">-Email</span></span>
<span data-ttu-id="1df2f-116">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="1df2f-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="1df2f-117">-FirstName</span></span>
<span data-ttu-id="1df2f-118">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="1df2f-119">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1df2f-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1df2f-120">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="1df2f-120">-LastName</span></span>
<span data-ttu-id="1df2f-121">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="1df2f-122">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1df2f-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1df2f-123">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="1df2f-123">-Note</span></span>
<span data-ttu-id="1df2f-124">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-124">Specifies a note about the user.</span></span>
<span data-ttu-id="1df2f-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1df2f-125">This parameter is optional.</span></span>
<span data-ttu-id="1df2f-126">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="1df2f-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="1df2f-127">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="1df2f-127">-Password</span></span>
<span data-ttu-id="1df2f-128">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="1df2f-128">Specifies the user password.</span></span>
<span data-ttu-id="1df2f-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="1df2f-129">This parameter is required.</span></span>

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

### <span data-ttu-id="1df2f-130">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="1df2f-130">-State</span></span>
<span data-ttu-id="1df2f-131">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-131">Specifies the user state.</span></span>
<span data-ttu-id="1df2f-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1df2f-132">This parameter is optional.</span></span>
<span data-ttu-id="1df2f-133">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="1df2f-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1df2f-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="1df2f-134">-UserId</span></span>
<span data-ttu-id="1df2f-135">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="1df2f-135">Specifies the user ID.</span></span>
<span data-ttu-id="1df2f-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1df2f-136">This parameter is optional.</span></span>
<span data-ttu-id="1df2f-137">Ha ez a paraméter nincs megadva, a parancsmag létrehoz egy felhasználói azonosítót.</span><span class="sxs-lookup"><span data-stu-id="1df2f-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="1df2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df2f-138">CommonParameters</span></span>
<span data-ttu-id="1df2f-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1df2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df2f-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df2f-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1df2f-141">INPUTS</span></span>

### <span data-ttu-id="1df2f-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1df2f-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1df2f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1df2f-143">System.String</span></span>

### <span data-ttu-id="1df2f-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1df2f-144">System.Security.SecureString</span></span>

### <span data-ttu-id="1df2f-145">System. nulla ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementUserState, Microsoft. Azure. PowerShell. parancsmagok. ApiManagement. ServiceManagement, Version = 1.0.0.0, = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1df2f-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1df2f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1df2f-146">OUTPUTS</span></span>

### <span data-ttu-id="1df2f-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1df2f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1df2f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1df2f-148">NOTES</span></span>

## <span data-ttu-id="1df2f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1df2f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1df2f-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1df2f-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="1df2f-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1df2f-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


