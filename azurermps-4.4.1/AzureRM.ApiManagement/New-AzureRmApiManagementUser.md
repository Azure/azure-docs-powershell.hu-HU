---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499279"
---
# <span data-ttu-id="f6348-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f6348-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="f6348-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6348-102">SYNOPSIS</span></span>
<span data-ttu-id="f6348-103">Új felhasználó regisztrálása.</span><span class="sxs-lookup"><span data-stu-id="f6348-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6348-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6348-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6348-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6348-105">DESCRIPTION</span></span>
<span data-ttu-id="f6348-106">A **New-AzureRmApiManagementUser** parancsmag új felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="f6348-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="f6348-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6348-107">EXAMPLES</span></span>

### <span data-ttu-id="f6348-108">1. példa: új felhasználó regisztrálása</span><span class="sxs-lookup"><span data-stu-id="f6348-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="f6348-109">Ez a parancs egy új, Patti Fuller nevű felhasználót regisztrál.</span><span class="sxs-lookup"><span data-stu-id="f6348-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="f6348-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6348-110">PARAMETERS</span></span>

### <span data-ttu-id="f6348-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f6348-111">-Context</span></span>
<span data-ttu-id="f6348-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f6348-113">– E-mail</span><span class="sxs-lookup"><span data-stu-id="f6348-113">-Email</span></span>
<span data-ttu-id="f6348-114">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="f6348-115">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="f6348-115">-FirstName</span></span>
<span data-ttu-id="f6348-116">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="f6348-117">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f6348-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f6348-118">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="f6348-118">-LastName</span></span>
<span data-ttu-id="f6348-119">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="f6348-120">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f6348-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f6348-121">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="f6348-121">-Note</span></span>
<span data-ttu-id="f6348-122">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-122">Specifies a note about the user.</span></span>
<span data-ttu-id="f6348-123">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f6348-123">This parameter is optional.</span></span>
<span data-ttu-id="f6348-124">Az alapértelmezett érték $Null.</span><span class="sxs-lookup"><span data-stu-id="f6348-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="f6348-125">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="f6348-125">-Password</span></span>
<span data-ttu-id="f6348-126">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="f6348-126">Specifies the user password.</span></span>
<span data-ttu-id="f6348-127">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="f6348-127">This parameter is required.</span></span>

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

### <span data-ttu-id="f6348-128">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="f6348-128">-State</span></span>
<span data-ttu-id="f6348-129">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-129">Specifies the user state.</span></span>
<span data-ttu-id="f6348-130">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f6348-130">This parameter is optional.</span></span>
<span data-ttu-id="f6348-131">A paraméter alapértelmezett értéke $Null.</span><span class="sxs-lookup"><span data-stu-id="f6348-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6348-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="f6348-132">-UserId</span></span>
<span data-ttu-id="f6348-133">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6348-133">Specifies the user ID.</span></span>
<span data-ttu-id="f6348-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="f6348-134">This parameter is optional.</span></span>
<span data-ttu-id="f6348-135">Ha ez a paraméter nincs megadva, a parancsmag létrehoz egy felhasználói azonosítót.</span><span class="sxs-lookup"><span data-stu-id="f6348-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="f6348-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6348-136">-DefaultProfile</span></span>
<span data-ttu-id="f6348-137">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6348-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6348-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6348-138">CommonParameters</span></span>
<span data-ttu-id="f6348-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6348-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6348-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6348-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6348-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6348-141">INPUTS</span></span>

## <span data-ttu-id="f6348-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6348-142">OUTPUTS</span></span>

### <span data-ttu-id="f6348-143">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f6348-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="f6348-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6348-144">NOTES</span></span>

## <span data-ttu-id="f6348-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6348-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6348-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f6348-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="f6348-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f6348-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


