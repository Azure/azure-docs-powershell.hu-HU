---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceVaultSecretGroupObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceVaultSecretGroupObject.md
ms.openlocfilehash: f4d45cddd893ece419fab38759425bb104b64522
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940585"
---
# <span data-ttu-id="aef6f-101">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="aef6f-101">New-AzCloudServiceVaultSecretGroupObject</span></span>

## <span data-ttu-id="aef6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aef6f-102">SYNOPSIS</span></span>
<span data-ttu-id="aef6f-103">Create a in-memory object for Vault Secret Group</span><span class="sxs-lookup"><span data-stu-id="aef6f-103">Create a in-memory object for Vault Secret Group</span></span>

## <span data-ttu-id="aef6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aef6f-104">SYNTAX</span></span>

```
New-AzCloudServiceVaultSecretGroupObject [-CertificateUrl <String[]>] [-Id <String>] [<CommonParameters>]
```

## <span data-ttu-id="aef6f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aef6f-105">DESCRIPTION</span></span>
<span data-ttu-id="aef6f-106">Create a in-memory object for Secret Group</span><span class="sxs-lookup"><span data-stu-id="aef6f-106">Create a in-memory object for Secret Group</span></span>

## <span data-ttu-id="aef6f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aef6f-107">EXAMPLES</span></span>

### <span data-ttu-id="aef6f-108">1. példa: Titkos csoportobjektum létrehozása a tárolóban</span><span class="sxs-lookup"><span data-stu-id="aef6f-108">Example 1: Create vault secret group object</span></span>
```powershell
$keyVault = Get-AzKeyVault -VaultName 'ContosoKeyVault'
$certificate = Get-AzKeyVaultCertificate -VaultName 'ContosoKeyVault' -Name 'ContosoCert'
$secretGroup = New-AzCloudServiceVaultSecretGroupObject -Id $keyVault.ResourceId -CertificateUrl $certificate.SecretId
```

<span data-ttu-id="aef6f-109">Ez a parancs egy titkos tárolócsoport-objektumot hoz létre, amely egy felhőszolgáltatás létrehozására vagy frissítésére használható.</span><span class="sxs-lookup"><span data-stu-id="aef6f-109">This command creates vault secret group object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="aef6f-110">További részletekért lásd: New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="aef6f-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="aef6f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aef6f-111">PARAMETERS</span></span>

### <span data-ttu-id="aef6f-112">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="aef6f-112">-CertificateUrl</span></span>
<span data-ttu-id="aef6f-113">Ez annak a tanúsítványnak az URL-címe, amely titkosként lett feltöltve a kulcstárolóba.</span><span class="sxs-lookup"><span data-stu-id="aef6f-113">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aef6f-114">-Id</span><span class="sxs-lookup"><span data-stu-id="aef6f-114">-Id</span></span>
<span data-ttu-id="aef6f-115">Kulcstár erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="aef6f-115">Key Vault Resource Id.</span></span>

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

### <span data-ttu-id="aef6f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aef6f-116">CommonParameters</span></span>
<span data-ttu-id="aef6f-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aef6f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aef6f-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aef6f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aef6f-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aef6f-119">INPUTS</span></span>

## <span data-ttu-id="aef6f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aef6f-120">OUTPUTS</span></span>

### <span data-ttu-id="aef6f-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span><span class="sxs-lookup"><span data-stu-id="aef6f-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceVaultSecretGroup</span></span>

## <span data-ttu-id="aef6f-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aef6f-122">NOTES</span></span>

<span data-ttu-id="aef6f-123">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aef6f-123">ALIASES</span></span>

## <span data-ttu-id="aef6f-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aef6f-124">RELATED LINKS</span></span>

