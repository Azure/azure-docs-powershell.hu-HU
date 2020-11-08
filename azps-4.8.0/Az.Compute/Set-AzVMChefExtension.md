---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMChefExtension.md
ms.openlocfilehash: 2821e9404fe4101415aa04a8b0d331b3066563df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182415"
---
# <span data-ttu-id="f5431-101">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5431-101">Set-AzVMChefExtension</span></span>

## <span data-ttu-id="f5431-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5431-102">SYNOPSIS</span></span>
<span data-ttu-id="f5431-103">Kibővíti a séf kiterjesztését egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f5431-103">Adds a Chef extension to a virtual machine.</span></span>

## <span data-ttu-id="f5431-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5431-104">SYNTAX</span></span>

### <span data-ttu-id="f5431-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f5431-105">Linux</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5431-106">Windows</span><span class="sxs-lookup"><span data-stu-id="f5431-106">Windows</span></span>
```
Set-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5431-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5431-107">DESCRIPTION</span></span>
<span data-ttu-id="f5431-108">A **set-AzVMChefExtension** parancsmag hozzáadja a Chef bővítményt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f5431-108">The **Set-AzVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="f5431-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f5431-109">EXAMPLES</span></span>

### <span data-ttu-id="f5431-110">1. példa: Chef-kiterjesztés hozzáadása Windows Virtual Machine-géphez</span><span class="sxs-lookup"><span data-stu-id="f5431-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="f5431-111">Ez a parancs egy WindowsVM001 nevű Windows Virtual Machine-bővítményt ad hozzá a Szakácshoz.</span><span class="sxs-lookup"><span data-stu-id="f5431-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="f5431-112">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="f5431-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f5431-113">2. példa: Chef-kiterjesztés hozzáadása egy linuxos virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="f5431-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="f5431-114">Ez a parancs hozzáadja a Chef bővítményt egy LinuxVM001 nevű linuxos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="f5431-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="f5431-115">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="f5431-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="f5431-116">3. példa: a Chef Extension bővítmény felvétele Windows Virtual Machine-be bootstrap beállításokkal</span><span class="sxs-lookup"><span data-stu-id="f5431-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="f5431-117">Ez a parancs hozzáadja a Chef kiterjesztését egy WindowsVM002 nevű Windows Virtual Machine-géphez.</span><span class="sxs-lookup"><span data-stu-id="f5431-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="f5431-118">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="f5431-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="f5431-119">A rendszerindítás után a virtuális gép a JSON formátumban megadott BootstrapOptions hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="f5431-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="f5431-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5431-120">PARAMETERS</span></span>

### <span data-ttu-id="f5431-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f5431-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="f5431-122">-BootstrapOptions</span></span>
<span data-ttu-id="f5431-123">A client_rb beállítás beállítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-123">Specifies configuration settings in the client_rb option.</span></span>

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

### <span data-ttu-id="f5431-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="f5431-124">-BootstrapVersion</span></span>
<span data-ttu-id="f5431-125">A bootstrap-konfiguráció verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-125">Specifies the version of the bootstrap configuration.</span></span>

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

### <span data-ttu-id="f5431-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="f5431-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="f5431-127">Annak gyakoriságát adja meg (percben), amikor a séf-szolgáltatás fut.</span><span class="sxs-lookup"><span data-stu-id="f5431-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="f5431-128">Ha abban az esetben, ha nem szeretné, hogy a séf-szolgáltatás telepítve legyen az Azure VM-ben, akkor ebben a mezőben a 0 értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="f5431-129">-ChefServerUrl</span></span>
<span data-ttu-id="f5431-130">A séf-kiszolgáló hivatkozását adja meg URL-címként.</span><span class="sxs-lookup"><span data-stu-id="f5431-130">Specifies the Chef server link, as a URL.</span></span>

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

### <span data-ttu-id="f5431-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="f5431-131">-ClientRb</span></span>
<span data-ttu-id="f5431-132">A Chef Client. RB teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-132">Specifies the full path of the Chef client.rb.</span></span>

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

### <span data-ttu-id="f5431-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="f5431-133">-Daemon</span></span>
<span data-ttu-id="f5431-134">A Chef-Client szolgáltatás beállítása felügyelet nélküli végrehajtáshoz.</span><span class="sxs-lookup"><span data-stu-id="f5431-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="f5431-135">A csomópont platformjának Windows rendszernek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f5431-135">The node platform should be Windows.</span></span>
<span data-ttu-id="f5431-136">Engedélyezett beállítások: "nincs", "szolgáltatás" és "tevékenység".</span><span class="sxs-lookup"><span data-stu-id="f5431-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="f5431-137">nincs – ez a beállítás megakadályozza a Chef-Client szolgáltatás szolgáltatásként való konfigurálását.</span><span class="sxs-lookup"><span data-stu-id="f5431-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="f5431-138">szolgáltatás – beállítja a séf – ügyfelet, hogy szolgáltatásként automatikusan fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="f5431-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="f5431-139">feladat – úgy állítja be a Chef-clientt, hogy a háttérben automatikusan fusson az ütemezett tevékenységként.</span><span class="sxs-lookup"><span data-stu-id="f5431-139">task - Configures the chef-client to run automatically in the background as a scheduled task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5431-140">-DefaultProfile</span></span>
<span data-ttu-id="f5431-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5431-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5431-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="f5431-142">-JsonAttribute</span></span>
<span data-ttu-id="f5431-143">A Chef-Client első futtatásához hozzáadni kívánt JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="f5431-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="f5431-144">például-JsonAttribute ' {"foo": "sáv"} '</span><span class="sxs-lookup"><span data-stu-id="f5431-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

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

### <span data-ttu-id="f5431-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="f5431-145">-Linux</span></span>
<span data-ttu-id="f5431-146">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="f5431-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-147">-Hely</span><span class="sxs-lookup"><span data-stu-id="f5431-147">-Location</span></span>
<span data-ttu-id="f5431-148">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5431-149">-Name</span></span>
<span data-ttu-id="f5431-150">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-151">-Várva</span><span class="sxs-lookup"><span data-stu-id="f5431-151">-NoWait</span></span>
<span data-ttu-id="f5431-152">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="f5431-152">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f5431-153">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="f5431-153">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-154">-Szervezetnév</span><span class="sxs-lookup"><span data-stu-id="f5431-154">-OrganizationName</span></span>
<span data-ttu-id="f5431-155">A séf-kiterjesztés szervezeti nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-155">Specifies the organization name of the Chef extension.</span></span>

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

### <span data-ttu-id="f5431-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5431-156">-ResourceGroupName</span></span>
<span data-ttu-id="f5431-157">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-157">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-158">-RunList</span><span class="sxs-lookup"><span data-stu-id="f5431-158">-RunList</span></span>
<span data-ttu-id="f5431-159">A Chef Node Run (sorozat) lista.</span><span class="sxs-lookup"><span data-stu-id="f5431-159">Specifies the Chef node run list.</span></span>

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

### <span data-ttu-id="f5431-160">-Secret</span><span class="sxs-lookup"><span data-stu-id="f5431-160">-Secret</span></span>
<span data-ttu-id="f5431-161">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcs.</span><span class="sxs-lookup"><span data-stu-id="f5431-161">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f5431-162">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="f5431-162">-SecretFile</span></span>
<span data-ttu-id="f5431-163">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcsot tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f5431-163">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

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

### <span data-ttu-id="f5431-164">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f5431-164">-TypeHandlerVersion</span></span>
<span data-ttu-id="f5431-165">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="f5431-165">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-166">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="f5431-166">-ValidationClientName</span></span>
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

### <span data-ttu-id="f5431-167">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="f5431-167">-ValidationPem</span></span>
<span data-ttu-id="f5431-168">A Chef validator. PEM fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-168">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="f5431-169">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5431-169">-VMName</span></span>
<span data-ttu-id="f5431-170">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-170">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f5431-171">Ez a parancsmag hozzáadja a Chef bővítményt a virtuális géphez, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="f5431-171">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-172">-Windows</span><span class="sxs-lookup"><span data-stu-id="f5431-172">-Windows</span></span>
<span data-ttu-id="f5431-173">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="f5431-173">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-174">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f5431-174">-Confirm</span></span>
<span data-ttu-id="f5431-175">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f5431-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5431-176">-WhatIf</span></span>
<span data-ttu-id="f5431-177">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f5431-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5431-178">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f5431-178">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5431-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5431-179">CommonParameters</span></span>
<span data-ttu-id="f5431-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5431-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5431-181">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5431-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5431-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5431-182">INPUTS</span></span>

### <span data-ttu-id="f5431-183">System. String</span><span class="sxs-lookup"><span data-stu-id="f5431-183">System.String</span></span>

### <span data-ttu-id="f5431-184">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5431-184">System.Boolean</span></span>

## <span data-ttu-id="f5431-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5431-185">OUTPUTS</span></span>

### <span data-ttu-id="f5431-186">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5431-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f5431-187">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5431-187">NOTES</span></span>

## <span data-ttu-id="f5431-188">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5431-188">RELATED LINKS</span></span>

[<span data-ttu-id="f5431-189">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5431-189">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="f5431-190">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f5431-190">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)
