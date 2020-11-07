---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836902"
---
# <span data-ttu-id="1f338-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1f338-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="1f338-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f338-102">SYNOPSIS</span></span>
<span data-ttu-id="1f338-103">Módosítja az API-kezelés tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="1f338-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="1f338-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f338-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f338-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f338-105">DESCRIPTION</span></span>
<span data-ttu-id="1f338-106">A **set-AzApiManagementProperty** parancsmag egy Azure API-kezelési tulajdonságot módosít.</span><span class="sxs-lookup"><span data-stu-id="1f338-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="1f338-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f338-107">EXAMPLES</span></span>

### <span data-ttu-id="1f338-108">Példa 1: a címkék módosítása egy tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="1f338-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="1f338-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="1f338-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="1f338-110">A második parancs módosítja az azonosító Property11 tartalmazó tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="1f338-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="1f338-111">A parancs a karakterláncokat a tulajdonságban címkékként rendeli $Tags.</span><span class="sxs-lookup"><span data-stu-id="1f338-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="1f338-112">2. példa: tulajdonság módosítása titkos érték megváltoztatásához</span><span class="sxs-lookup"><span data-stu-id="1f338-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="1f338-113">A parancs a titkosított tulajdonságot módosítja.</span><span class="sxs-lookup"><span data-stu-id="1f338-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="1f338-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f338-114">PARAMETERS</span></span>

### <span data-ttu-id="1f338-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1f338-115">-Context</span></span>
<span data-ttu-id="1f338-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1f338-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f338-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f338-117">-DefaultProfile</span></span>
<span data-ttu-id="1f338-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f338-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f338-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f338-119">-Name</span></span>
<span data-ttu-id="1f338-120">A tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f338-120">Specifies the name of the property.</span></span>
<span data-ttu-id="1f338-121">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="1f338-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="1f338-122">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="1f338-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="1f338-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f338-123">-PassThru</span></span>
<span data-ttu-id="1f338-124">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementProperty** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1f338-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1f338-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="1f338-125">-PropertyId</span></span>
<span data-ttu-id="1f338-126">A parancsmag által módosított tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f338-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1f338-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="1f338-127">-Secret</span></span>
<span data-ttu-id="1f338-128">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1f338-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f338-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="1f338-129">-Tag</span></span>
<span data-ttu-id="1f338-130">Tulajdonsággal társított Címkék</span><span class="sxs-lookup"><span data-stu-id="1f338-130">Tags associated with a property.</span></span> <span data-ttu-id="1f338-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1f338-131">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f338-132">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="1f338-132">-Value</span></span>
<span data-ttu-id="1f338-133">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f338-133">Specifies a value for the property.</span></span>
<span data-ttu-id="1f338-134">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="1f338-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="1f338-135">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="1f338-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="1f338-136">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="1f338-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="1f338-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f338-137">CommonParameters</span></span>
<span data-ttu-id="1f338-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f338-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f338-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f338-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f338-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f338-140">INPUTS</span></span>

### <span data-ttu-id="1f338-141">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f338-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f338-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1f338-142">System.String</span></span>

### <span data-ttu-id="1f338-143">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f338-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f338-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="1f338-144">System.String[]</span></span>

### <span data-ttu-id="1f338-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f338-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1f338-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f338-146">OUTPUTS</span></span>

### <span data-ttu-id="1f338-147">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1f338-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="1f338-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f338-148">NOTES</span></span>

## <span data-ttu-id="1f338-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f338-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f338-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1f338-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="1f338-151">Új – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1f338-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="1f338-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1f338-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


