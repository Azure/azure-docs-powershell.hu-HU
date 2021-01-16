---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347285"
---
# <span data-ttu-id="0c7e9-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="0c7e9-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="0c7e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7e9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7e9-103">Létrehozhatja vagy frissítheti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="0c7e9-104">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="0c7e9-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c7e9-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c7e9-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c7e9-106">DESCRIPTION</span></span>
<span data-ttu-id="0c7e9-107">Létrehozhatja vagy frissítheti egy Windows IoT-eszközszolgáltatás metaadatait.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="0c7e9-108">A tulajdonság módosításának szokásos sémája az, hogy beolvassa a Windows IoT eszközszolgáltatás metaadatait és biztonsági metaadatait, majd kombinálja őket a módosított értékekkel egy új törzsben a Windows IoT eszközszolgáltatás frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="0c7e9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c7e9-109">EXAMPLES</span></span>

### <span data-ttu-id="0c7e9-110">1. példa: Új Windows IoT-szolgáltatás létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c7e9-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="0c7e9-111">Ez a parancs új Windows IoT-szolgáltatásokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="0c7e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7e9-112">PARAMETERS</span></span>

### <span data-ttu-id="0c7e9-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="0c7e9-113">-AdminDomainName</span></span>
<span data-ttu-id="0c7e9-114">Windows IoT eszközszolgáltatás OEM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="0c7e9-114">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="0c7e9-115">-BillingDomainName</span></span>
<span data-ttu-id="0c7e9-116">Windows IoT-eszközszolgáltatás – ODM AAD-tartomány</span><span class="sxs-lookup"><span data-stu-id="0c7e9-116">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7e9-117">-DefaultProfile</span></span>
<span data-ttu-id="0c7e9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="0c7e9-119">-Etag</span></span>
<span data-ttu-id="0c7e9-120">Az Etag mező nem *kötelező.*</span><span class="sxs-lookup"><span data-stu-id="0c7e9-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="0c7e9-121">Ha a válasz törzsében meg van biztosítanak, a normál ETag-konvenciónak megfelelő fejlécként is meg kell azt adni.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="0c7e9-122">-IfMatch</span></span>
<span data-ttu-id="0c7e9-123">A Windows IoT eszközszolgáltatás Etagja.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="0c7e9-124">Ne adjon meg új Windows IoT-eszközszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="0c7e9-125">Egy meglévő Windows IoT-eszközszolgáltatás frissítéséhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-125">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-126">-Location</span><span class="sxs-lookup"><span data-stu-id="0c7e9-126">-Location</span></span>
<span data-ttu-id="0c7e9-127">Az azure-régió, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="0c7e9-127">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0c7e9-128">-Name</span></span>
<span data-ttu-id="0c7e9-129">A Windows IoT-eszközszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-130">-Note</span><span class="sxs-lookup"><span data-stu-id="0c7e9-130">-Note</span></span>
<span data-ttu-id="0c7e9-131">A Windows IoT-eszközszolgáltatás megjegyzései.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-131">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-132">-Mennyiség</span><span class="sxs-lookup"><span data-stu-id="0c7e9-132">-Quantity</span></span>
<span data-ttu-id="0c7e9-133">Windows IoT-eszközszolgáltatás eszközfoglalása,</span><span class="sxs-lookup"><span data-stu-id="0c7e9-133">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7e9-134">-ResourceGroupName</span></span>
<span data-ttu-id="0c7e9-135">A Windows IoT eszközszolgáltatást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c7e9-136">-SubscriptionId</span></span>
<span data-ttu-id="0c7e9-137">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c7e9-138">-Tag</span></span>
<span data-ttu-id="0c7e9-139">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-139">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7e9-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c7e9-140">-Confirm</span></span>
<span data-ttu-id="0c7e9-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7e9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7e9-142">-WhatIf</span></span>
<span data-ttu-id="0c7e9-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7e9-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7e9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7e9-145">CommonParameters</span></span>
<span data-ttu-id="0c7e9-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7e9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7e9-147">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7e9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7e9-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7e9-148">INPUTS</span></span>

## <span data-ttu-id="0c7e9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c7e9-149">OUTPUTS</span></span>

### <span data-ttu-id="0c7e9-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="0c7e9-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="0c7e9-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c7e9-151">NOTES</span></span>

<span data-ttu-id="0c7e9-152">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0c7e9-152">ALIASES</span></span>

## <span data-ttu-id="0c7e9-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c7e9-153">RELATED LINKS</span></span>

