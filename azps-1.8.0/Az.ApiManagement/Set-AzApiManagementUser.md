---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: 03ea39c24166b6e44c057907fbc7346996d3dfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836895"
---
# <span data-ttu-id="b8ada-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b8ada-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="b8ada-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8ada-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ada-103">Felhasználói adatok megadása</span><span class="sxs-lookup"><span data-stu-id="b8ada-103">Sets user details.</span></span>

## <span data-ttu-id="b8ada-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8ada-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ada-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8ada-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ada-106">A **set-AzApiManagementUser** parancsmag felhasználói adatokat állít be.</span><span class="sxs-lookup"><span data-stu-id="b8ada-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="b8ada-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8ada-107">EXAMPLES</span></span>

### <span data-ttu-id="b8ada-108">Példa 1: felhasználó jelszavának, e-mail-címének és állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="b8ada-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="b8ada-109">Ez a parancs új felhasználói jelszót és e-mail-címet állít be, és blokkolja a felhasználót.</span><span class="sxs-lookup"><span data-stu-id="b8ada-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="b8ada-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8ada-110">PARAMETERS</span></span>

### <span data-ttu-id="b8ada-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b8ada-111">-Context</span></span>
<span data-ttu-id="b8ada-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b8ada-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b8ada-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b8ada-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ada-114">-DefaultProfile</span></span>
<span data-ttu-id="b8ada-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8ada-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8ada-116">– E-mail</span><span class="sxs-lookup"><span data-stu-id="b8ada-116">-Email</span></span>
<span data-ttu-id="b8ada-117">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="b8ada-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b8ada-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8ada-119">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="b8ada-119">-FirstName</span></span>
<span data-ttu-id="b8ada-120">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="b8ada-121">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b8ada-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="b8ada-122">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="b8ada-122">-LastName</span></span>
<span data-ttu-id="b8ada-123">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="b8ada-124">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="b8ada-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="b8ada-125">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="b8ada-125">-Note</span></span>
<span data-ttu-id="b8ada-126">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-126">Specifies a note about the user.</span></span>
<span data-ttu-id="b8ada-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b8ada-127">This parameter is optional.</span></span>
<span data-ttu-id="b8ada-128">A paraméter alapértelmezett értéke $null.</span><span class="sxs-lookup"><span data-stu-id="b8ada-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="b8ada-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8ada-129">-PassThru</span></span>
<span data-ttu-id="b8ada-130">passthru</span><span class="sxs-lookup"><span data-stu-id="b8ada-130">passthru</span></span>

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

### <span data-ttu-id="b8ada-131">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b8ada-131">-Password</span></span>
<span data-ttu-id="b8ada-132">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="b8ada-132">Specifies the user password.</span></span>
<span data-ttu-id="b8ada-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b8ada-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ada-134">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="b8ada-134">-State</span></span>
<span data-ttu-id="b8ada-135">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-135">Specifies the user state.</span></span>
<span data-ttu-id="b8ada-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b8ada-136">This parameter is optional.</span></span>
<span data-ttu-id="b8ada-137">Az alapértelmezett érték aktív.</span><span class="sxs-lookup"><span data-stu-id="b8ada-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ada-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="b8ada-138">-UserId</span></span>
<span data-ttu-id="b8ada-139">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8ada-139">Specifies the user ID.</span></span>
<span data-ttu-id="b8ada-140">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="b8ada-140">This parameter is required.</span></span>

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

### <span data-ttu-id="b8ada-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ada-141">CommonParameters</span></span>
<span data-ttu-id="b8ada-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8ada-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ada-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ada-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ada-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8ada-144">INPUTS</span></span>

### <span data-ttu-id="b8ada-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8ada-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b8ada-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ada-146">System.String</span></span>

### <span data-ttu-id="b8ada-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b8ada-147">System.Security.SecureString</span></span>

### <span data-ttu-id="b8ada-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="b8ada-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="b8ada-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b8ada-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b8ada-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8ada-150">OUTPUTS</span></span>

### <span data-ttu-id="b8ada-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b8ada-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="b8ada-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8ada-152">NOTES</span></span>

## <span data-ttu-id="b8ada-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8ada-153">RELATED LINKS</span></span>

[<span data-ttu-id="b8ada-154">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b8ada-154">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="b8ada-155">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b8ada-155">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="b8ada-156">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b8ada-156">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


