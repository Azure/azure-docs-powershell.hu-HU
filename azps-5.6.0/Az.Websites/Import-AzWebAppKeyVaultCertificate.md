---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007414"
---
# <span data-ttu-id="0ce33-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0ce33-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="0ce33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ce33-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce33-103">Importálja az SSL-tanúsítványt egy webalkalmazásba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="0ce33-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="0ce33-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ce33-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ce33-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ce33-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce33-106">Az **Import-AzWebAppKeyVaultCertificate** parancsmag ssl-tanúsítványt importál egy webappba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="0ce33-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="0ce33-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ce33-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce33-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ce33-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="0ce33-109">Ez a parancs egy SSL-tanúsítványt importál egy webalkalmazásba a kulcstárolóból.</span><span class="sxs-lookup"><span data-stu-id="0ce33-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="0ce33-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="0ce33-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="0ce33-111">Ez a parancs SSL-tanúsítvány importálása webalkalmazásba a kulcstárolóból erőforrás-azonosító használatával (általában ha a kulcstár egy másik előfizetésben található).</span><span class="sxs-lookup"><span data-stu-id="0ce33-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="0ce33-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ce33-112">PARAMETERS</span></span>

### <span data-ttu-id="0ce33-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="0ce33-113">-CertName</span></span>
<span data-ttu-id="0ce33-114">KeyVaultCertName a keyvaultban létrehozott tanúsítványhoz</span><span class="sxs-lookup"><span data-stu-id="0ce33-114">KeyVaultCertName of the certificate created in keyvault</span></span>

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

### <span data-ttu-id="0ce33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce33-115">-DefaultProfile</span></span>
<span data-ttu-id="0ce33-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ce33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ce33-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="0ce33-117">-KeyVaultName</span></span>
<span data-ttu-id="0ce33-118">A billentyűk neve.</span><span class="sxs-lookup"><span data-stu-id="0ce33-118">The name of the keyvault.</span></span>

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

### <span data-ttu-id="0ce33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce33-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ce33-120">A webapp erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ce33-120">The name of the webapp resource group.</span></span>

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

### <span data-ttu-id="0ce33-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="0ce33-121">-Slot</span></span>
<span data-ttu-id="0ce33-122">A webapphely neve.</span><span class="sxs-lookup"><span data-stu-id="0ce33-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="0ce33-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="0ce33-123">-WebAppName</span></span>
<span data-ttu-id="0ce33-124">A webapp neve.</span><span class="sxs-lookup"><span data-stu-id="0ce33-124">The name of the webapp.</span></span>

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

### <span data-ttu-id="0ce33-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ce33-125">-Confirm</span></span>
<span data-ttu-id="0ce33-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ce33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce33-127">-WhatIf</span></span>
<span data-ttu-id="0ce33-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ce33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce33-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ce33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce33-130">CommonParameters</span></span>
<span data-ttu-id="0ce33-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ce33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce33-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce33-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce33-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ce33-133">INPUTS</span></span>

### <span data-ttu-id="0ce33-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ce33-134">None</span></span>

## <span data-ttu-id="0ce33-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ce33-135">OUTPUTS</span></span>

### <span data-ttu-id="0ce33-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="0ce33-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="0ce33-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ce33-137">NOTES</span></span>

## <span data-ttu-id="0ce33-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ce33-138">RELATED LINKS</span></span>
