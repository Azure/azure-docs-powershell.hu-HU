---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672497"
---
# <span data-ttu-id="42f1b-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42f1b-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="42f1b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="42f1b-103">Új felhasználó regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="42f1b-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42f1b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42f1b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f1b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="42f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="42f1b-106">A **New-AzureRmApiManagementUser** parancsmag új felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="42f1b-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="42f1b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="42f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="42f1b-108">1. példa: új felhasználó regisztrálása</span><span class="sxs-lookup"><span data-stu-id="42f1b-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="42f1b-109">Ez a parancs egy új, Patti Fuller nevű felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="42f1b-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="42f1b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42f1b-110">PARAMETERS</span></span>

### <span data-ttu-id="42f1b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="42f1b-111">-Context</span></span>
<span data-ttu-id="42f1b-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="42f1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f1b-113">-DefaultProfile</span></span>
<span data-ttu-id="42f1b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42f1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f1b-115">– E-mail</span><span class="sxs-lookup"><span data-stu-id="42f1b-115">-Email</span></span>
<span data-ttu-id="42f1b-116">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="42f1b-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="42f1b-117">-FirstName</span></span>
<span data-ttu-id="42f1b-118">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="42f1b-119">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="42f1b-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="42f1b-120">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="42f1b-120">-LastName</span></span>
<span data-ttu-id="42f1b-121">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="42f1b-122">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="42f1b-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="42f1b-123">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="42f1b-123">-Note</span></span>
<span data-ttu-id="42f1b-124">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-124">Specifies a note about the user.</span></span>
<span data-ttu-id="42f1b-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="42f1b-125">This parameter is optional.</span></span>
<span data-ttu-id="42f1b-126">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="42f1b-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="42f1b-127">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="42f1b-127">-Password</span></span>
<span data-ttu-id="42f1b-128">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="42f1b-128">Specifies the user password.</span></span>
<span data-ttu-id="42f1b-129">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="42f1b-129">This parameter is required.</span></span>

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

### <span data-ttu-id="42f1b-130">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="42f1b-130">-State</span></span>
<span data-ttu-id="42f1b-131">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-131">Specifies the user state.</span></span>
<span data-ttu-id="42f1b-132">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="42f1b-132">This parameter is optional.</span></span>
<span data-ttu-id="42f1b-133">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="42f1b-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="42f1b-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="42f1b-134">-UserId</span></span>
<span data-ttu-id="42f1b-135">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="42f1b-135">Specifies the user ID.</span></span>
<span data-ttu-id="42f1b-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="42f1b-136">This parameter is optional.</span></span>
<span data-ttu-id="42f1b-137">Ha ez a paraméter nincs megadva, a parancsmag létrehoz egy felhasználói azonosítót.</span><span class="sxs-lookup"><span data-stu-id="42f1b-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="42f1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f1b-138">CommonParameters</span></span>
<span data-ttu-id="42f1b-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42f1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f1b-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f1b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f1b-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42f1b-141">INPUTS</span></span>

### <span data-ttu-id="42f1b-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42f1b-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42f1b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="42f1b-143">System.String</span></span>

### <span data-ttu-id="42f1b-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="42f1b-144">System.Security.SecureString</span></span>

### <span data-ttu-id="42f1b-145">System. null ' 1 [[Microsoft. Azure. commands. ApiManagement. ServiceManagement. models. PsApiManagementUserState, Microsoft. Azure. commands. ApiManagement. ServiceManagement, Version = 6.1.0.0</span><span class="sxs-lookup"><span data-stu-id="42f1b-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="42f1b-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42f1b-146">OUTPUTS</span></span>

### <span data-ttu-id="42f1b-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42f1b-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="42f1b-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42f1b-148">NOTES</span></span>

## <span data-ttu-id="42f1b-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42f1b-149">RELATED LINKS</span></span>

[<span data-ttu-id="42f1b-150">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42f1b-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="42f1b-151">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="42f1b-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


