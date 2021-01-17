---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480717"
---
# <span data-ttu-id="6e43f-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6e43f-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="6e43f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e43f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e43f-103">Beállítja a lemeztitkosítási kulcs tulajdonságait egy lemezfrissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="6e43f-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="6e43f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e43f-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e43f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e43f-105">DESCRIPTION</span></span>
<span data-ttu-id="6e43f-106">A **Set-AzDiskUpdateDiskEncryptionKey** parancsmag beállítja a lemeztitkosítási kulcs tulajdonságait egy lemezfrissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="6e43f-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="6e43f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e43f-107">EXAMPLES</span></span>

### <span data-ttu-id="6e43f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e43f-108">Example 1</span></span>
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

<span data-ttu-id="6e43f-109">Az első parancs egy 10 GB-os helyi üres lemezfrissítési objektumot hoz létre Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="6e43f-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6e43f-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="6e43f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6e43f-111">A második és a harmadik parancs a lemezfrissítési objektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e43f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="6e43f-112">Az utolsó parancs átveszi a lemezfrissítési objektumot, és frissíti a "Disk01" nevű meglévő lemez nevét az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="6e43f-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6e43f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e43f-113">PARAMETERS</span></span>

### <span data-ttu-id="6e43f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e43f-114">-DefaultProfile</span></span>
<span data-ttu-id="6e43f-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e43f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e43f-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="6e43f-116">-DiskUpdate</span></span>
<span data-ttu-id="6e43f-117">Helyi lemezfrissítési objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6e43f-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="6e43f-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="6e43f-118">-SecretUrl</span></span>
<span data-ttu-id="6e43f-119">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e43f-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="6e43f-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6e43f-120">-SourceVaultId</span></span>
<span data-ttu-id="6e43f-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e43f-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="6e43f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e43f-122">-Confirm</span></span>
<span data-ttu-id="6e43f-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e43f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e43f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e43f-124">-WhatIf</span></span>
<span data-ttu-id="6e43f-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e43f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e43f-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e43f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e43f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e43f-127">CommonParameters</span></span>
<span data-ttu-id="6e43f-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e43f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e43f-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e43f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e43f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e43f-130">INPUTS</span></span>

### <span data-ttu-id="6e43f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="6e43f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="6e43f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6e43f-132">System.String</span></span>

## <span data-ttu-id="6e43f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e43f-133">OUTPUTS</span></span>

### <span data-ttu-id="6e43f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="6e43f-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="6e43f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e43f-135">NOTES</span></span>

## <span data-ttu-id="6e43f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e43f-136">RELATED LINKS</span></span>
