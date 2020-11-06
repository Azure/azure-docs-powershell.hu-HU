---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492589"
---
# <span data-ttu-id="54064-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54064-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="54064-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54064-102">SYNOPSIS</span></span>
<span data-ttu-id="54064-103">Felhasználói adatok megadása</span><span class="sxs-lookup"><span data-stu-id="54064-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54064-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54064-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54064-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54064-105">DESCRIPTION</span></span>
<span data-ttu-id="54064-106">A **set-AzureRmApiManagementUser** parancsmag felhasználói adatokat állít be.</span><span class="sxs-lookup"><span data-stu-id="54064-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="54064-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54064-107">EXAMPLES</span></span>

### <span data-ttu-id="54064-108">Példa 1: felhasználó jelszavának, e-mail-címének és állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="54064-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="54064-109">Ez a parancs új felhasználói jelszót és e-mail-címet állít be, és blokkolja a felhasználót.</span><span class="sxs-lookup"><span data-stu-id="54064-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="54064-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54064-110">PARAMETERS</span></span>

### <span data-ttu-id="54064-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="54064-111">-Context</span></span>
<span data-ttu-id="54064-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="54064-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="54064-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54064-113">This parameter is required.</span></span>

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

### <span data-ttu-id="54064-114">– E-mail</span><span class="sxs-lookup"><span data-stu-id="54064-114">-Email</span></span>
<span data-ttu-id="54064-115">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="54064-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="54064-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="54064-117">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="54064-117">-FirstName</span></span>
<span data-ttu-id="54064-118">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="54064-119">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="54064-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="54064-120">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="54064-120">-LastName</span></span>
<span data-ttu-id="54064-121">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="54064-122">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="54064-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="54064-123">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="54064-123">-Note</span></span>
<span data-ttu-id="54064-124">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-124">Specifies a note about the user.</span></span>
<span data-ttu-id="54064-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="54064-125">This parameter is optional.</span></span>
<span data-ttu-id="54064-126">A paraméter alapértelmezett értéke $null.</span><span class="sxs-lookup"><span data-stu-id="54064-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="54064-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54064-127">-PassThru</span></span>
<span data-ttu-id="54064-128">passthru</span><span class="sxs-lookup"><span data-stu-id="54064-128">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54064-129">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="54064-129">-Password</span></span>
<span data-ttu-id="54064-130">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="54064-130">Specifies the user password.</span></span>
<span data-ttu-id="54064-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="54064-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="54064-132">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="54064-132">-State</span></span>
<span data-ttu-id="54064-133">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-133">Specifies the user state.</span></span>
<span data-ttu-id="54064-134">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="54064-134">This parameter is optional.</span></span>
<span data-ttu-id="54064-135">Az alapértelmezett érték aktív.</span><span class="sxs-lookup"><span data-stu-id="54064-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54064-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="54064-136">-UserId</span></span>
<span data-ttu-id="54064-137">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="54064-137">Specifies the user ID.</span></span>
<span data-ttu-id="54064-138">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="54064-138">This parameter is required.</span></span>

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

### <span data-ttu-id="54064-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54064-139">-DefaultProfile</span></span>
<span data-ttu-id="54064-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54064-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54064-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54064-141">CommonParameters</span></span>
<span data-ttu-id="54064-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54064-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54064-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54064-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54064-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54064-144">INPUTS</span></span>

## <span data-ttu-id="54064-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54064-145">OUTPUTS</span></span>

### <span data-ttu-id="54064-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54064-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="54064-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54064-147">NOTES</span></span>

## <span data-ttu-id="54064-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54064-148">RELATED LINKS</span></span>

[<span data-ttu-id="54064-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54064-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="54064-150">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54064-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="54064-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="54064-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


