---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: d3825b4887d2361a4bb378bfddc3085773efd84b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503899"
---
# <span data-ttu-id="95fe0-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="95fe0-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="95fe0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="95fe0-103">Felhasználói adatok megadása</span><span class="sxs-lookup"><span data-stu-id="95fe0-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95fe0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95fe0-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95fe0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="95fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="95fe0-106">A **set-AzureRmApiManagementUser** parancsmag felhasználói adatokat állít be.</span><span class="sxs-lookup"><span data-stu-id="95fe0-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="95fe0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="95fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="95fe0-108">Példa 1: felhasználó jelszavának, e-mail-címének és állapotának módosítása</span><span class="sxs-lookup"><span data-stu-id="95fe0-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="95fe0-109">Ez a parancs új felhasználói jelszót és e-mail-címet állít be, és blokkolja a felhasználót.</span><span class="sxs-lookup"><span data-stu-id="95fe0-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="95fe0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95fe0-110">PARAMETERS</span></span>

### <span data-ttu-id="95fe0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="95fe0-111">-Context</span></span>
<span data-ttu-id="95fe0-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="95fe0-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="95fe0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="95fe0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fe0-114">-DefaultProfile</span></span>
<span data-ttu-id="95fe0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95fe0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="95fe0-116">– E-mail</span><span class="sxs-lookup"><span data-stu-id="95fe0-116">-Email</span></span>
<span data-ttu-id="95fe0-117">A felhasználó e-mail-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="95fe0-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="95fe0-118">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-119">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="95fe0-119">-FirstName</span></span>
<span data-ttu-id="95fe0-120">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="95fe0-121">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="95fe0-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-122">-Vezetéknév</span><span class="sxs-lookup"><span data-stu-id="95fe0-122">-LastName</span></span>
<span data-ttu-id="95fe0-123">A felhasználó vezetéknevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="95fe0-124">A paraméternek 1 – 100 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="95fe0-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-125">-Megjegyzés</span><span class="sxs-lookup"><span data-stu-id="95fe0-125">-Note</span></span>
<span data-ttu-id="95fe0-126">A felhasználó megjegyzését adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-126">Specifies a note about the user.</span></span>
<span data-ttu-id="95fe0-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="95fe0-127">This parameter is optional.</span></span>
<span data-ttu-id="95fe0-128">A paraméter alapértelmezett értéke $null.</span><span class="sxs-lookup"><span data-stu-id="95fe0-128">The default value of this parameter is $null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95fe0-129">-PassThru</span></span>
<span data-ttu-id="95fe0-130">passthru</span><span class="sxs-lookup"><span data-stu-id="95fe0-130">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-131">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="95fe0-131">-Password</span></span>
<span data-ttu-id="95fe0-132">Megadja a felhasználó jelszavát.</span><span class="sxs-lookup"><span data-stu-id="95fe0-132">Specifies the user password.</span></span>
<span data-ttu-id="95fe0-133">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="95fe0-133">This parameter is optional.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-134">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="95fe0-134">-State</span></span>
<span data-ttu-id="95fe0-135">A felhasználói állapotot adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-135">Specifies the user state.</span></span>
<span data-ttu-id="95fe0-136">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="95fe0-136">This parameter is optional.</span></span>
<span data-ttu-id="95fe0-137">Az alapértelmezett érték aktív.</span><span class="sxs-lookup"><span data-stu-id="95fe0-137">The default value is Active.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="95fe0-138">-UserId</span></span>
<span data-ttu-id="95fe0-139">A felhasználói azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="95fe0-139">Specifies the user ID.</span></span>
<span data-ttu-id="95fe0-140">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="95fe0-140">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95fe0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fe0-141">CommonParameters</span></span>
<span data-ttu-id="95fe0-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95fe0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fe0-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fe0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fe0-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95fe0-144">INPUTS</span></span>

### <span data-ttu-id="95fe0-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="95fe0-145">None</span></span>
<span data-ttu-id="95fe0-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="95fe0-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95fe0-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95fe0-147">OUTPUTS</span></span>

### <span data-ttu-id="95fe0-148">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="95fe0-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="95fe0-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95fe0-149">NOTES</span></span>

## <span data-ttu-id="95fe0-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95fe0-150">RELATED LINKS</span></span>

[<span data-ttu-id="95fe0-151">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="95fe0-151">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="95fe0-152">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="95fe0-152">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="95fe0-153">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="95fe0-153">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


