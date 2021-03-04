---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: b87dbef98f336d1171da4b33d4ced1cc86e04fdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922441"
---
# <span data-ttu-id="d6067-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d6067-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="d6067-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6067-102">SYNOPSIS</span></span>
<span data-ttu-id="d6067-103">Beállítja a kulcstitkosítási kulcs tulajdonságait egy pillanatfelvételi frissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="d6067-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="d6067-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6067-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6067-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6067-105">DESCRIPTION</span></span>
<span data-ttu-id="d6067-106">A **Set-AzSnapshotUpdateKeyEncryptionKey** parancsmag beállítja a kulcstitkosítási kulcs tulajdonságait egy pillanatfelvételi frissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="d6067-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="d6067-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6067-107">EXAMPLES</span></span>

### <span data-ttu-id="d6067-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d6067-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="d6067-109">Az első parancs létrehoz egy 10 GB-os helyi üres pillanatkép-frissítő objektumot Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="d6067-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d6067-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="d6067-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d6067-111">A második és a harmadik parancs a lemeztitkosítási kulcs és a kulcstitkosítási kulcs beállításait adja meg a pillanatfelvételi frissítési objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d6067-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d6067-112">Az utolsó parancs az "Erőforráscsoport01" erőforráscsoport "Snapshot01" nevű pillanatképét frissíti a pillanatkép-frissítő objektummal.</span><span class="sxs-lookup"><span data-stu-id="d6067-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d6067-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6067-113">PARAMETERS</span></span>

### <span data-ttu-id="d6067-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6067-114">-DefaultProfile</span></span>
<span data-ttu-id="d6067-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6067-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6067-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d6067-116">-KeyUrl</span></span>
<span data-ttu-id="d6067-117">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6067-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="d6067-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d6067-118">-SnapshotUpdate</span></span>
<span data-ttu-id="d6067-119">Helyi pillanatkép-frissítő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6067-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6067-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d6067-120">-SourceVaultId</span></span>
<span data-ttu-id="d6067-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6067-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d6067-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6067-122">-Confirm</span></span>
<span data-ttu-id="d6067-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d6067-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6067-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6067-124">-WhatIf</span></span>
<span data-ttu-id="d6067-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d6067-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6067-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6067-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6067-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6067-127">CommonParameters</span></span>
<span data-ttu-id="d6067-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6067-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6067-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6067-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6067-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6067-130">INPUTS</span></span>

### <span data-ttu-id="d6067-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d6067-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="d6067-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d6067-132">System.String</span></span>

## <span data-ttu-id="d6067-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6067-133">OUTPUTS</span></span>

### <span data-ttu-id="d6067-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d6067-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="d6067-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6067-135">NOTES</span></span>

## <span data-ttu-id="d6067-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6067-136">RELATED LINKS</span></span>
