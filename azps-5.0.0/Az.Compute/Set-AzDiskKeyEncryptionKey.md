---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 6f2037b638b8fd055ef79ca6a8502a17bd5f7911
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187510"
---
# <span data-ttu-id="b1873-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b1873-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="b1873-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1873-102">SYNOPSIS</span></span>
<span data-ttu-id="b1873-103">A kulcs titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="b1873-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="b1873-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1873-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1873-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1873-105">DESCRIPTION</span></span>
<span data-ttu-id="b1873-106">A **set-AzDiskKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be a Disk objektumban.</span><span class="sxs-lookup"><span data-stu-id="b1873-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="b1873-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1873-107">EXAMPLES</span></span>

### <span data-ttu-id="b1873-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b1873-108">Example 1</span></span>
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

<span data-ttu-id="b1873-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="b1873-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b1873-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="b1873-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b1873-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1873-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="b1873-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="b1873-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b1873-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1873-113">PARAMETERS</span></span>

### <span data-ttu-id="b1873-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1873-114">-DefaultProfile</span></span>
<span data-ttu-id="b1873-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1873-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1873-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="b1873-116">-Disk</span></span>
<span data-ttu-id="b1873-117">Helyi lemez-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="b1873-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="b1873-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="b1873-118">-KeyUrl</span></span>
<span data-ttu-id="b1873-119">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1873-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="b1873-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="b1873-120">-SourceVaultId</span></span>
<span data-ttu-id="b1873-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1873-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="b1873-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1873-122">-Confirm</span></span>
<span data-ttu-id="b1873-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1873-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1873-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1873-124">-WhatIf</span></span>
<span data-ttu-id="b1873-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1873-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1873-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1873-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1873-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1873-127">CommonParameters</span></span>
<span data-ttu-id="b1873-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1873-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1873-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1873-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1873-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1873-130">INPUTS</span></span>

### <span data-ttu-id="b1873-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b1873-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="b1873-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b1873-132">System.String</span></span>

## <span data-ttu-id="b1873-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1873-133">OUTPUTS</span></span>

### <span data-ttu-id="b1873-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b1873-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b1873-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1873-135">NOTES</span></span>

## <span data-ttu-id="b1873-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1873-136">RELATED LINKS</span></span>