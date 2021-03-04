---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 4a130755b4cfd84b0394d51c7dcf65b0437925e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919009"
---
# <span data-ttu-id="9477e-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9477e-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="9477e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9477e-102">SYNOPSIS</span></span>
<span data-ttu-id="9477e-103">Beállítja a kulcstitkosítási kulcs tulajdonságait egy lemezobjektumon.</span><span class="sxs-lookup"><span data-stu-id="9477e-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="9477e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9477e-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9477e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9477e-105">DESCRIPTION</span></span>
<span data-ttu-id="9477e-106">A **Set-AzDiskKeyEncryptionKey** parancsmag beállítja a lemezobjektumok kulcstitkosítási kulcs tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="9477e-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="9477e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9477e-107">EXAMPLES</span></span>

### <span data-ttu-id="9477e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9477e-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="9477e-109">Az első parancs egy 5 GB-os helyi üres lemezobjektumot hoz létre Standard_LRS tárfióktípusban.</span><span class="sxs-lookup"><span data-stu-id="9477e-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="9477e-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="9477e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9477e-111">A második és a harmadik parancs a lemezobjektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="9477e-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="9477e-112">Az utolsó parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="9477e-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9477e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9477e-113">PARAMETERS</span></span>

### <span data-ttu-id="9477e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9477e-114">-DefaultProfile</span></span>
<span data-ttu-id="9477e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9477e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9477e-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="9477e-116">-Disk</span></span>
<span data-ttu-id="9477e-117">Helyi lemezobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9477e-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9477e-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="9477e-118">-KeyUrl</span></span>
<span data-ttu-id="9477e-119">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9477e-119">Specifies the key Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9477e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9477e-120">-SourceVaultId</span></span>
<span data-ttu-id="9477e-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9477e-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9477e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9477e-122">-Confirm</span></span>
<span data-ttu-id="9477e-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9477e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9477e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9477e-124">-WhatIf</span></span>
<span data-ttu-id="9477e-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9477e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9477e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9477e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9477e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9477e-127">CommonParameters</span></span>
<span data-ttu-id="9477e-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9477e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9477e-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9477e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9477e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9477e-130">INPUTS</span></span>

### <span data-ttu-id="9477e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9477e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="9477e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9477e-132">System.String</span></span>

## <span data-ttu-id="9477e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9477e-133">OUTPUTS</span></span>

### <span data-ttu-id="9477e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9477e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="9477e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9477e-135">NOTES</span></span>

## <span data-ttu-id="9477e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9477e-136">RELATED LINKS</span></span>
