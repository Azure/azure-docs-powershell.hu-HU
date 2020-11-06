---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492900"
---
# <span data-ttu-id="a8989-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8989-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="a8989-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8989-102">SYNOPSIS</span></span>
<span data-ttu-id="a8989-103">Felhasználói adatok megadása</span><span class="sxs-lookup"><span data-stu-id="a8989-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8989-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8989-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8989-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8989-105">DESCRIPTION</span></span>
<span data-ttu-id="a8989-106">A **set-AzureRmApiManagementUser** parancsmag felhasználói adatokat állít be.</span><span class="sxs-lookup"><span data-stu-id="a8989-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="a8989-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a8989-107">EXAMPLES</span></span>

### <span data-ttu-id="a8989-108">Példa 1: felhasználó jelszavának, e-mail-címének és állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="a8989-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="a8989-109">Ez a parancs új felhasználói jelszót és e-mail-címet állít be, és blokkolja a felhasználót.</span><span class="sxs-lookup"><span data-stu-id="a8989-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="a8989-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8989-110">PARAMETERS</span></span>

### <span data-ttu-id="a8989-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a8989-111">-Context</span></span>
<span data-ttu-id="a8989-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a8989-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a8989-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a8989-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8989-114">-DefaultProfile</span></span>
<span data-ttu-id="a8989-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8989-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8989-116">– E-mail</span><span class="sxs-lookup"><span data-stu-id="a8989-116">-Email</span></span>
<span data-ttu-id="a8989-117">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="a8989-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a8989-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="a8989-119">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="a8989-119">-FirstName</span></span>
<span data-ttu-id="a8989-120">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="a8989-121">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a8989-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a8989-122">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="a8989-122">-LastName</span></span>
<span data-ttu-id="a8989-123">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="a8989-124">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a8989-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a8989-125">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="a8989-125">-Note</span></span>
<span data-ttu-id="a8989-126">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-126">Specifies a note about the user.</span></span>
<span data-ttu-id="a8989-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a8989-127">This parameter is optional.</span></span>
<span data-ttu-id="a8989-128">A paraméter alapértelmezett értéke $null.</span><span class="sxs-lookup"><span data-stu-id="a8989-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="a8989-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8989-129">-PassThru</span></span>
<span data-ttu-id="a8989-130">passthru</span><span class="sxs-lookup"><span data-stu-id="a8989-130">passthru</span></span>

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

### <span data-ttu-id="a8989-131">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="a8989-131">-Password</span></span>
<span data-ttu-id="a8989-132">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="a8989-132">Specifies the user password.</span></span>
<span data-ttu-id="a8989-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a8989-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="a8989-134">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="a8989-134">-State</span></span>
<span data-ttu-id="a8989-135">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-135">Specifies the user state.</span></span>
<span data-ttu-id="a8989-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="a8989-136">This parameter is optional.</span></span>
<span data-ttu-id="a8989-137">Az alapértelmezett érték aktív.</span><span class="sxs-lookup"><span data-stu-id="a8989-137">The default value is Active.</span></span>

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

### <span data-ttu-id="a8989-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="a8989-138">-UserId</span></span>
<span data-ttu-id="a8989-139">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8989-139">Specifies the user ID.</span></span>
<span data-ttu-id="a8989-140">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="a8989-140">This parameter is required.</span></span>

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

### <span data-ttu-id="a8989-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8989-141">CommonParameters</span></span>
<span data-ttu-id="a8989-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8989-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8989-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8989-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8989-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8989-144">INPUTS</span></span>

### <span data-ttu-id="a8989-145">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a8989-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8989-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a8989-146">System.String</span></span>

### <span data-ttu-id="a8989-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a8989-147">System.Security.SecureString</span></span>

### <span data-ttu-id="a8989-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="a8989-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="a8989-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8989-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8989-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8989-150">OUTPUTS</span></span>

### <span data-ttu-id="a8989-151">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8989-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="a8989-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8989-152">NOTES</span></span>

## <span data-ttu-id="a8989-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8989-153">RELATED LINKS</span></span>

[<span data-ttu-id="a8989-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8989-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="a8989-155">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8989-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="a8989-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a8989-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


