---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: bb60ce1fc2cb20a24d1b445cf4a3729bf26747ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925337"
---
# <span data-ttu-id="2b555-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2b555-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="2b555-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b555-102">SYNOPSIS</span></span>
<span data-ttu-id="2b555-103">Módosít egy API-kezelési tanúsítványt, amely a háttérprogrammal történő közös hitelesítéshez van konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="2b555-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="2b555-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2b555-104">SYNTAX</span></span>

### <span data-ttu-id="2b555-105">LoadFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2b555-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b555-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="2b555-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b555-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2b555-107">DESCRIPTION</span></span>
<span data-ttu-id="2b555-108">A **Set-AzApiManagementCertificate** parancsmag módosítja az Azure API Management tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2b555-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="2b555-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2b555-109">EXAMPLES</span></span>

### <span data-ttu-id="2b555-110">1. példa: Tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="2b555-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="2b555-111">Ez a parancs módosítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="2b555-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="2b555-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b555-112">PARAMETERS</span></span>

### <span data-ttu-id="2b555-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2b555-113">-CertificateId</span></span>
<span data-ttu-id="2b555-114">A módosítani szükséges tanúsítvány azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2b555-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="2b555-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2b555-115">-Context</span></span>
<span data-ttu-id="2b555-116">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="2b555-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b555-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b555-117">-DefaultProfile</span></span>
<span data-ttu-id="2b555-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2b555-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b555-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b555-119">-PassThru</span></span>
<span data-ttu-id="2b555-120">passthru</span><span class="sxs-lookup"><span data-stu-id="2b555-120">passthru</span></span>

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

### <span data-ttu-id="2b555-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="2b555-121">-PfxBytes</span></span>
<span data-ttu-id="2b555-122">A tanúsítványfájl bájttömbje .pfx formátumban.</span><span class="sxs-lookup"><span data-stu-id="2b555-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="2b555-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2b555-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b555-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="2b555-124">-PfxFilePath</span></span>
<span data-ttu-id="2b555-125">A tanúsítványfájl .pfx formátumú elérési útját adja meg a létrehozáshoz és a feltöltéshez.</span><span class="sxs-lookup"><span data-stu-id="2b555-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="2b555-126">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2b555-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b555-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="2b555-127">-PfxPassword</span></span>
<span data-ttu-id="2b555-128">Megadja a tanúsítvány jelszavát.</span><span class="sxs-lookup"><span data-stu-id="2b555-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="2b555-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b555-129">CommonParameters</span></span>
<span data-ttu-id="2b555-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b555-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b555-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b555-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b555-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b555-132">INPUTS</span></span>

### <span data-ttu-id="2b555-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b555-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b555-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2b555-134">System.String</span></span>

### <span data-ttu-id="2b555-135">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="2b555-135">System.Byte[]</span></span>

### <span data-ttu-id="2b555-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b555-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2b555-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b555-137">OUTPUTS</span></span>

### <span data-ttu-id="2b555-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2b555-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="2b555-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2b555-139">NOTES</span></span>

## <span data-ttu-id="2b555-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b555-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b555-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2b555-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="2b555-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2b555-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="2b555-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2b555-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


