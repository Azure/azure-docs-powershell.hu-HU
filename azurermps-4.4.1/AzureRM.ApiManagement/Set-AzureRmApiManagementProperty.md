---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492590"
---
# <span data-ttu-id="2e3ad-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2e3ad-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="2e3ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3ad-103">Módosítja az API-kezelés tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e3ad-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e3ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e3ad-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3ad-106">A **set-AzureRmApiManagementProperty** parancsmag egy Azure API-kezelési tulajdonságot módosít.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="2e3ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e3ad-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3ad-108">Példa 1: a címkék módosítása egy tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="2e3ad-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="2e3ad-109">Az első parancs két értéket rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="2e3ad-110">A második parancs módosítja az azonosító Property11 tartalmazó tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="2e3ad-111">A parancs a karakterláncokat a tulajdonságban címkékként rendeli $Tags.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="2e3ad-112">2. példa: tulajdonság módosítása titkos érték megváltoztatásához</span><span class="sxs-lookup"><span data-stu-id="2e3ad-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="2e3ad-113">A parancs a titkosított tulajdonságot módosítja.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="2e3ad-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e3ad-114">PARAMETERS</span></span>

### <span data-ttu-id="2e3ad-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2e3ad-115">-Context</span></span>
<span data-ttu-id="2e3ad-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e3ad-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e3ad-117">-Name</span></span>
<span data-ttu-id="2e3ad-118">A tulajdonság nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-118">Specifies the name of the property.</span></span>
<span data-ttu-id="2e3ad-119">A maximális hossz 100 karakter.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-119">Maximum length is 100 characters.</span></span>
<span data-ttu-id="2e3ad-120">A nevek csak betűket, számokat, pont-, kötőjel-és aláhúzás karaktereket tartalmaznak.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-120">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="2e3ad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e3ad-121">-PassThru</span></span>
<span data-ttu-id="2e3ad-122">Jelzi, hogy ez a parancsmag a parancsmag által módosított **PsApiManagementProperty** adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-122">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2e3ad-123">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="2e3ad-123">-PropertyId</span></span>
<span data-ttu-id="2e3ad-124">A parancsmag által módosított tulajdonság AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-124">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2e3ad-125">-Secret</span><span class="sxs-lookup"><span data-stu-id="2e3ad-125">-Secret</span></span>
<span data-ttu-id="2e3ad-126">Azt jelzi, hogy a tulajdonság értéke titkos, ezért titkosítottnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-126">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="2e3ad-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2e3ad-127">-Tags</span></span>
<span data-ttu-id="2e3ad-128">A parancsmag által a tulajdonsághoz társított címkék tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-128">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="2e3ad-129">Címkék használatával szűrheti a tulajdonságokat tartalmazó listát.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-129">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="2e3ad-130">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="2e3ad-130">-Value</span></span>
<span data-ttu-id="2e3ad-131">A tulajdonság értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-131">Specifies a value for the property.</span></span>
<span data-ttu-id="2e3ad-132">Ez az érték tartalmazhat házirend-kifejezéseket.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-132">This value can contain policy expressions.</span></span>
<span data-ttu-id="2e3ad-133">A maximális hossz 1000 karakter.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-133">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="2e3ad-134">Lehet, hogy az érték nem üres, vagy csak szóközökből áll.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-134">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="2e3ad-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3ad-135">-DefaultProfile</span></span>
<span data-ttu-id="2e3ad-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e3ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3ad-137">CommonParameters</span></span>
<span data-ttu-id="2e3ad-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e3ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3ad-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3ad-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3ad-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3ad-140">INPUTS</span></span>

## <span data-ttu-id="2e3ad-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3ad-141">OUTPUTS</span></span>

### <span data-ttu-id="2e3ad-142">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2e3ad-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="2e3ad-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e3ad-143">NOTES</span></span>

## <span data-ttu-id="2e3ad-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e3ad-144">RELATED LINKS</span></span>

[<span data-ttu-id="2e3ad-145">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2e3ad-145">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="2e3ad-146">Új – AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2e3ad-146">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="2e3ad-147">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="2e3ad-147">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


