---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: ccd19f0390957466f9fb799d3655aa8bb1d02d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667919"
---
# <span data-ttu-id="407ba-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="407ba-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="407ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="407ba-102">SYNOPSIS</span></span>
<span data-ttu-id="407ba-103">Felhasználói adatok megadása</span><span class="sxs-lookup"><span data-stu-id="407ba-103">Sets user details.</span></span>

## <span data-ttu-id="407ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="407ba-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="407ba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="407ba-105">DESCRIPTION</span></span>
<span data-ttu-id="407ba-106">A **set-AzApiManagementUser** parancsmag felhasználói adatokat állít be.</span><span class="sxs-lookup"><span data-stu-id="407ba-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="407ba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="407ba-107">EXAMPLES</span></span>

### <span data-ttu-id="407ba-108">Példa 1: felhasználó jelszavának, e-mail-címének és állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="407ba-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="407ba-109">Ez a parancs új felhasználói jelszót és e-mail-címet állít be, és blokkolja a felhasználót.</span><span class="sxs-lookup"><span data-stu-id="407ba-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="407ba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="407ba-110">PARAMETERS</span></span>

### <span data-ttu-id="407ba-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="407ba-111">-Context</span></span>
<span data-ttu-id="407ba-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="407ba-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="407ba-113">This parameter is required.</span></span>

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

### <span data-ttu-id="407ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407ba-114">-DefaultProfile</span></span>
<span data-ttu-id="407ba-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="407ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="407ba-116">– E-mail</span><span class="sxs-lookup"><span data-stu-id="407ba-116">-Email</span></span>
<span data-ttu-id="407ba-117">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="407ba-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="407ba-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="407ba-119">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="407ba-119">-FirstName</span></span>
<span data-ttu-id="407ba-120">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="407ba-121">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="407ba-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="407ba-122">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="407ba-122">-LastName</span></span>
<span data-ttu-id="407ba-123">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="407ba-124">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="407ba-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="407ba-125">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="407ba-125">-Note</span></span>
<span data-ttu-id="407ba-126">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-126">Specifies a note about the user.</span></span>
<span data-ttu-id="407ba-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="407ba-127">This parameter is optional.</span></span>
<span data-ttu-id="407ba-128">A paraméter alapértelmezett értéke $null.</span><span class="sxs-lookup"><span data-stu-id="407ba-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="407ba-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="407ba-129">-PassThru</span></span>
<span data-ttu-id="407ba-130">passthru</span><span class="sxs-lookup"><span data-stu-id="407ba-130">passthru</span></span>

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

### <span data-ttu-id="407ba-131">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="407ba-131">-Password</span></span>
<span data-ttu-id="407ba-132">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="407ba-132">Specifies the user password.</span></span>
<span data-ttu-id="407ba-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="407ba-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="407ba-134">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="407ba-134">-State</span></span>
<span data-ttu-id="407ba-135">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-135">Specifies the user state.</span></span>
<span data-ttu-id="407ba-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="407ba-136">This parameter is optional.</span></span>
<span data-ttu-id="407ba-137">Az alapértelmezett érték aktív.</span><span class="sxs-lookup"><span data-stu-id="407ba-137">The default value is Active.</span></span>

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

### <span data-ttu-id="407ba-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="407ba-138">-UserId</span></span>
<span data-ttu-id="407ba-139">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="407ba-139">Specifies the user ID.</span></span>
<span data-ttu-id="407ba-140">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="407ba-140">This parameter is required.</span></span>

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

### <span data-ttu-id="407ba-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="407ba-141">-Confirm</span></span>
<span data-ttu-id="407ba-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="407ba-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407ba-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="407ba-143">-WhatIf</span></span>
<span data-ttu-id="407ba-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="407ba-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="407ba-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="407ba-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="407ba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407ba-146">CommonParameters</span></span>
<span data-ttu-id="407ba-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="407ba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407ba-148">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="407ba-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407ba-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="407ba-149">INPUTS</span></span>

### <span data-ttu-id="407ba-150">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="407ba-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="407ba-151">System. String</span><span class="sxs-lookup"><span data-stu-id="407ba-151">System.String</span></span>

### <span data-ttu-id="407ba-152">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="407ba-152">System.Security.SecureString</span></span>

### <span data-ttu-id="407ba-153">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="407ba-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="407ba-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="407ba-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="407ba-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="407ba-155">OUTPUTS</span></span>

### <span data-ttu-id="407ba-156">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="407ba-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="407ba-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="407ba-157">NOTES</span></span>

## <span data-ttu-id="407ba-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="407ba-158">RELATED LINKS</span></span>

[<span data-ttu-id="407ba-159">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="407ba-159">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="407ba-160">Új – AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="407ba-160">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="407ba-161">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="407ba-161">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


