---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 49b86055c185dd474499cf8674a34668f69ee060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667923"
---
# <span data-ttu-id="1be93-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be93-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="1be93-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1be93-102">SYNOPSIS</span></span>
<span data-ttu-id="1be93-103">Módosítja az API-kezelés tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="1be93-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="1be93-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1be93-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be93-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1be93-105">DESCRIPTION</span></span>
<span data-ttu-id="1be93-106">A **set-AzApiManagementProperty** parancsmag egy Azure API-kezelési tulajdonságot módosít.</span><span class="sxs-lookup"><span data-stu-id="1be93-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="1be93-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1be93-107">EXAMPLES</span></span>

### <span data-ttu-id="1be93-108">Példa 1: a címkék módosítása egy tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="1be93-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="1be93-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="1be93-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="1be93-110">A második parancs módosítja az azonosító Property11 tartalmazó tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="1be93-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="1be93-111">A parancs a karakterláncokat a tulajdonságban címkékként rendeli $Tags.</span><span class="sxs-lookup"><span data-stu-id="1be93-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="1be93-112">2. példa: tulajdonság módosítása titkos érték megváltoztatásához</span><span class="sxs-lookup"><span data-stu-id="1be93-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="1be93-113">A parancs a titkosított tulajdonságot módosítja.</span><span class="sxs-lookup"><span data-stu-id="1be93-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="1be93-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1be93-114">PARAMETERS</span></span>

### <span data-ttu-id="1be93-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1be93-115">-Context</span></span>
<span data-ttu-id="1be93-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1be93-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1be93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be93-117">-DefaultProfile</span></span>
<span data-ttu-id="1be93-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1be93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1be93-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1be93-119">-Name</span></span>
<span data-ttu-id="1be93-120">A tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1be93-120">Specifies the name of the property.</span></span>
<span data-ttu-id="1be93-121">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="1be93-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="1be93-122">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="1be93-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="1be93-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1be93-123">-PassThru</span></span>
<span data-ttu-id="1be93-124">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementProperty** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1be93-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1be93-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="1be93-125">-PropertyId</span></span>
<span data-ttu-id="1be93-126">A parancsmag által módosított tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1be93-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1be93-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="1be93-127">-Secret</span></span>
<span data-ttu-id="1be93-128">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1be93-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="1be93-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="1be93-129">-Tag</span></span>
<span data-ttu-id="1be93-130">Tulajdonsággal társított Címkék</span><span class="sxs-lookup"><span data-stu-id="1be93-130">Tags associated with a property.</span></span> <span data-ttu-id="1be93-131">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="1be93-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="1be93-132">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="1be93-132">-Value</span></span>
<span data-ttu-id="1be93-133">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1be93-133">Specifies a value for the property.</span></span>
<span data-ttu-id="1be93-134">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="1be93-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="1be93-135">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="1be93-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="1be93-136">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="1be93-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="1be93-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1be93-137">-Confirm</span></span>
<span data-ttu-id="1be93-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1be93-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1be93-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be93-139">-WhatIf</span></span>
<span data-ttu-id="1be93-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1be93-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1be93-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1be93-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1be93-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be93-142">CommonParameters</span></span>
<span data-ttu-id="1be93-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1be93-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be93-144">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1be93-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be93-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1be93-145">INPUTS</span></span>

### <span data-ttu-id="1be93-146">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1be93-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1be93-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1be93-147">System.String</span></span>

### <span data-ttu-id="1be93-148">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1be93-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1be93-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="1be93-149">System.String[]</span></span>

### <span data-ttu-id="1be93-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1be93-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1be93-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1be93-151">OUTPUTS</span></span>

### <span data-ttu-id="1be93-152">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be93-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="1be93-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1be93-153">NOTES</span></span>

## <span data-ttu-id="1be93-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1be93-154">RELATED LINKS</span></span>

[<span data-ttu-id="1be93-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be93-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="1be93-156">Új – AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be93-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="1be93-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="1be93-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


