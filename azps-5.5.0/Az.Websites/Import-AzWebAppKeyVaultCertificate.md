---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: 61f498a521134ee0abb74f45ff048c94e7c53081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157738"
---
# <span data-ttu-id="a1451-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a1451-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="a1451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1451-102">SYNOPSIS</span></span>
<span data-ttu-id="a1451-103">IMPORTÁLhat EGY SSL-tanúsítványt egy webalkalmazásba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="a1451-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="a1451-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1451-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1451-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1451-105">DESCRIPTION</span></span>
<span data-ttu-id="a1451-106">Az **Import-AzWebAppKeyVaultCertificate** parancsmag ssl-tanúsítványt importál egy webappba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="a1451-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="a1451-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1451-107">EXAMPLES</span></span>

### <span data-ttu-id="a1451-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a1451-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="a1451-109">Ez a parancs egy SSL-tanúsítványt importál egy webalkalmazásba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="a1451-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="a1451-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a1451-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="a1451-111">Ez a parancs SSL-tanúsítvány importálása webalkalmazásba a kulcstárolóból erőforrás-azonosító használatával (általában ha a kulcstár egy másik előfizetésben található).</span><span class="sxs-lookup"><span data-stu-id="a1451-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="a1451-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1451-112">PARAMETERS</span></span>

### <span data-ttu-id="a1451-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="a1451-113">-CertName</span></span>
<span data-ttu-id="a1451-114">KeyVaultCertName a keyvaultban létrehozott tanúsítványhoz</span><span class="sxs-lookup"><span data-stu-id="a1451-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1451-115">-DefaultProfile</span></span>
<span data-ttu-id="a1451-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1451-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1451-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="a1451-117">-KeyVaultName</span></span>
<span data-ttu-id="a1451-118">A billentyűk neve.</span><span class="sxs-lookup"><span data-stu-id="a1451-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1451-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1451-120">A webapp erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a1451-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="a1451-121">-Slot</span></span>
<span data-ttu-id="a1451-122">A webapphely neve.</span><span class="sxs-lookup"><span data-stu-id="a1451-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="a1451-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="a1451-123">-WebAppName</span></span>
<span data-ttu-id="a1451-124">A webapp neve.</span><span class="sxs-lookup"><span data-stu-id="a1451-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1451-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1451-125">-Confirm</span></span>
<span data-ttu-id="a1451-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a1451-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1451-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1451-127">-WhatIf</span></span>
<span data-ttu-id="a1451-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a1451-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1451-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1451-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1451-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1451-130">CommonParameters</span></span>
<span data-ttu-id="a1451-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1451-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1451-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1451-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1451-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1451-133">INPUTS</span></span>

### <span data-ttu-id="a1451-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="a1451-134">None</span></span>

## <span data-ttu-id="a1451-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1451-135">OUTPUTS</span></span>

### <span data-ttu-id="a1451-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="a1451-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="a1451-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1451-137">NOTES</span></span>

## <span data-ttu-id="a1451-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1451-138">RELATED LINKS</span></span>
