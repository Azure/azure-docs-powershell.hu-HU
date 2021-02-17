---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 73c765d35238d960a95b86c90ad2ff7f2cd5db11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209991"
---
# <span data-ttu-id="bfaad-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bfaad-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="bfaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfaad-102">SYNOPSIS</span></span>
<span data-ttu-id="bfaad-103">Beállítja a kulcstitkosítási kulcs tulajdonságait egy lemezfrissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="bfaad-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="bfaad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bfaad-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfaad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bfaad-105">DESCRIPTION</span></span>
<span data-ttu-id="bfaad-106">A **Set-AzDiskUpdateKeyEncryptionKey** parancsmag beállítja a kulcstitkosítási kulcs tulajdonságait egy lemezfrissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="bfaad-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="bfaad-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bfaad-107">EXAMPLES</span></span>

### <span data-ttu-id="bfaad-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bfaad-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="bfaad-109">Az első parancs egy 10 GB-os helyi üres lemezfrissítési objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="bfaad-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bfaad-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="bfaad-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="bfaad-111">A második és a harmadik parancs a lemezfrissítési objektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfaad-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="bfaad-112">Az utolsó parancs átveszi a lemezfrissítési objektumot, és frissíti a "Disk01" nevű meglévő lemez nevét az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="bfaad-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bfaad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfaad-113">PARAMETERS</span></span>

### <span data-ttu-id="bfaad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfaad-114">-DefaultProfile</span></span>
<span data-ttu-id="bfaad-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfaad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfaad-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bfaad-116">-DiskUpdate</span></span>
<span data-ttu-id="bfaad-117">Helyi lemezfrissítési objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bfaad-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfaad-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="bfaad-118">-KeyUrl</span></span>
<span data-ttu-id="bfaad-119">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfaad-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="bfaad-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="bfaad-120">-SourceVaultId</span></span>
<span data-ttu-id="bfaad-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bfaad-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="bfaad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfaad-122">-Confirm</span></span>
<span data-ttu-id="bfaad-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bfaad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfaad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfaad-124">-WhatIf</span></span>
<span data-ttu-id="bfaad-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bfaad-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfaad-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfaad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfaad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaad-127">CommonParameters</span></span>
<span data-ttu-id="bfaad-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfaad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaad-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfaad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaad-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bfaad-130">INPUTS</span></span>

### <span data-ttu-id="bfaad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bfaad-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="bfaad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="bfaad-132">System.String</span></span>

## <span data-ttu-id="bfaad-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfaad-133">OUTPUTS</span></span>

### <span data-ttu-id="bfaad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bfaad-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="bfaad-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bfaad-135">NOTES</span></span>

## <span data-ttu-id="bfaad-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfaad-136">RELATED LINKS</span></span>
