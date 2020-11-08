---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dc0d985203d51c705c40b423d0b6c9f381fa87e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011925"
---
# <span data-ttu-id="4bfda-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bfda-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="4bfda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bfda-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfda-103">Megkapja a megadott hatókör-házirendet.</span><span class="sxs-lookup"><span data-stu-id="4bfda-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="4bfda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bfda-104">SYNTAX</span></span>

### <span data-ttu-id="4bfda-105">GetTenantLevel (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4bfda-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bfda-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="4bfda-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4bfda-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="4bfda-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bfda-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="4bfda-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bfda-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bfda-109">DESCRIPTION</span></span>
<span data-ttu-id="4bfda-110">A **Get-AzApiManagementPolicy** parancsmag a megadott hatóköri házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="4bfda-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4bfda-111">EXAMPLES</span></span>

### <span data-ttu-id="4bfda-112">Példa 1: a bérlői szint házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bfda-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="4bfda-113">Ez a parancs bérlői szintű házirendet kap, és egy tenantpolicy.xml nevű fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="4bfda-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="4bfda-114">2. példa: a termékspecifikus házirend beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bfda-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="4bfda-115">Ez a parancs a Product-scope Policy házirendet kapja meg</span><span class="sxs-lookup"><span data-stu-id="4bfda-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="4bfda-116">3. példa: az API-hatókörök házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bfda-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="4bfda-117">Ez a parancs API-hatóköri házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="4bfda-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="4bfda-118">Példa 4: a művelet-hatókör házirendjének beszerzése</span><span class="sxs-lookup"><span data-stu-id="4bfda-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="4bfda-119">Ez a parancs a művelet hatóköre házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="4bfda-120">Példa 5: a bérlői hatókör házirendjének beszerzése RawXml formátumban</span><span class="sxs-lookup"><span data-stu-id="4bfda-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $context -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="4bfda-121">Ez a parancs a bérlői hatókörű házirendet a nem XML Escape formátumban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="4bfda-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bfda-122">PARAMETERS</span></span>

### <span data-ttu-id="4bfda-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4bfda-123">-ApiId</span></span>
<span data-ttu-id="4bfda-124">A meglévő API azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="4bfda-125">Ha ezt a paramétert adja meg, a parancsmag az API-scope házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4bfda-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfda-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4bfda-126">-ApiRevision</span></span>
<span data-ttu-id="4bfda-127">Az API-módosítás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4bfda-127">Identifier of API Revision.</span></span> <span data-ttu-id="4bfda-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="4bfda-128">This parameter is optional.</span></span> <span data-ttu-id="4bfda-129">Ha nem adja meg, akkor a rendszer az aktuális API-verzióból olvassa be a házirendet.</span><span class="sxs-lookup"><span data-stu-id="4bfda-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfda-130">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4bfda-130">-Context</span></span>
<span data-ttu-id="4bfda-131">A **PsApiManagementContext** példányát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4bfda-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bfda-132">-DefaultProfile</span></span>
<span data-ttu-id="4bfda-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bfda-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bfda-134">-Force</span><span class="sxs-lookup"><span data-stu-id="4bfda-134">-Force</span></span>
<span data-ttu-id="4bfda-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="4bfda-135">ps_force</span></span>

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

### <span data-ttu-id="4bfda-136">Formátumú</span><span class="sxs-lookup"><span data-stu-id="4bfda-136">-Format</span></span>
<span data-ttu-id="4bfda-137">Az API-kezelési házirend formátumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="4bfda-138">A paraméter alapértelmezett értéke "XML".</span><span class="sxs-lookup"><span data-stu-id="4bfda-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="4bfda-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4bfda-139">-OperationId</span></span>
<span data-ttu-id="4bfda-140">A meglévő API-művelet azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="4bfda-141">Ha ezt a paramétert a *ApiId* -ban adja meg, a parancsmag a műveleti hatókör házirendjét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4bfda-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfda-142">-Termékkód</span><span class="sxs-lookup"><span data-stu-id="4bfda-142">-ProductId</span></span>
<span data-ttu-id="4bfda-143">Egy meglévő szorzat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4bfda-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="4bfda-144">Ha ezt a paramétert adja meg, a parancsmag a termékspecifikus házirendet adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="4bfda-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bfda-145">-Saven</span><span class="sxs-lookup"><span data-stu-id="4bfda-145">-SaveAs</span></span>
<span data-ttu-id="4bfda-146">Annak a fájlnak az elérési útját adja meg, ahová menteni szeretné az eredményt.</span><span class="sxs-lookup"><span data-stu-id="4bfda-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="4bfda-147">Ha nem adja meg ezt a paramétert, az eredmény a folyamat csípése.</span><span class="sxs-lookup"><span data-stu-id="4bfda-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="4bfda-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4bfda-148">-Confirm</span></span>
<span data-ttu-id="4bfda-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bfda-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bfda-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bfda-150">-WhatIf</span></span>
<span data-ttu-id="4bfda-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4bfda-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bfda-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bfda-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bfda-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfda-153">CommonParameters</span></span>
<span data-ttu-id="4bfda-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bfda-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfda-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4bfda-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfda-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bfda-156">INPUTS</span></span>

### <span data-ttu-id="4bfda-157">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4bfda-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4bfda-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4bfda-158">System.String</span></span>

### <span data-ttu-id="4bfda-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4bfda-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4bfda-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bfda-160">OUTPUTS</span></span>

### <span data-ttu-id="4bfda-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4bfda-161">System.String</span></span>

## <span data-ttu-id="4bfda-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bfda-162">NOTES</span></span>

## <span data-ttu-id="4bfda-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bfda-163">RELATED LINKS</span></span>

[<span data-ttu-id="4bfda-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bfda-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="4bfda-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="4bfda-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


